---
title: Improved Permalink Redirection
author: Tyler Longren
type: post
date: 2006-08-19T05:15:34+00:00
url: /improved-permalink-redirection/
DiggURL:
  - http://digg.com/programming/Google_Safe_URL_Redirection
wjt_diPostTopic:
  - programming
ratings_users:
  - 1
ratings_score:
  - 5
ratings_average:
  - 5
views:
  - 6939
dsq_thread_id:
  - 1385921496
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - code
  - coding
  - css
  - development
  - howto
  - Internet
  - Personal
  - PHP
  - php-code
  - php-scripts
  - redirect
  - scripts
  - useful
  - WordPress
  - www

---
After a hard evenings work, I have a much better redirection method to replace [the one I described in this post][1]. Previously, I was simply guessing which post a searcher was looking for and displayed a link to that post.

That was all fine and dandy, but I have pretty good search ranking for various keywords. I&#8217;d like to keep it that way. After digging around a bit I came across the best method to keep my search rankings in place and manage to redirect the searcher to the desired post. Enter the 301 Permanent Redirect.

I found a [nice simple PHP function to do redirection][2] on any number of levels. This function has the ability to send specific HTTP/1.1 status codes based on the type of redirection desired. Since my old permalinks will never be valid again, I chose the 301 Permanent Redirect. **A note**, the function listed at the URL linked above doesn&#8217;t work as-is, you need to modify it. The modified function is below, plus some extra code. All of that code is in my themes header.php file.  
<!--more-->

<pre><?php
$uri = $_SERVER[REQUEST_URI];
$uri = explode("/",$uri);
$dir = $uri[1];
$postid = $uri[2];
if ($dir == "archives" &#038;&#038; $postid != "") {
	function redirect($to,$code=301) {
	$location = null;
	$sn = $_SERVER['SCRIPT_NAME'];
	$cp = dirname($sn);
	if (substr($to,0,4)=='http') $location = $to; // Absolute URL
	else
	{
	  $schema = $_SERVER['SERVER_PORT']=='443'?'https':'http';
	  $host = strlen($_SERVER['HTTP_HOST'])?$_SERVER['HTTP_HOST']:$_SERVER['SERVER_NAME'];
	  if (substr($to,0,1)=='/') $location = "$schema://$host$to";
	  elseif (substr($to,0,1)=='.') // Relative Path
	  {
	    $location = "$schema://$host/";
	    $pu = parse_url($to);
	    $cd = dirname($_SERVER['SCRIPT_FILENAME']).'/';
	    $np = realpath($cd.$pu['path']);
	    $np = str_replace($_SERVER['DOCUMENT_ROOT'],'',$np);
	    $location.= $np;
	    if ((isset($pu['query'])) &#038;&#038; (strlen($pu['query'])>0)) $location.= '?'.$pu['query'];
	  }
	}

	$hs = headers_sent($filename, $linenum);
	if ($hs==false)
	{
	  if ($code==301) header("HTTP/1.1 301 Moved Permanently"); // Convert to GET
	  elseif ($code==302) header("HTTP/1.1 302 Found"); // Conform re-POST
	  elseif ($code==303) header("HTTP/1.1 303 See Other"); // dont cache, always use GET
	  elseif ($code==304) header("HTTP/1.1 304 Not Modified"); // use cache
	  elseif ($code==305) header("HTTP/1.1 305 Use Proxy");
	  elseif ($code==306) header("HTTP/1.1 306 Not Used");
	  elseif ($code==307) header("HTTP/1.1 307 Temorary Redirect");
	  else trigger_error("Unhandled redirect() HTTP Code: $code",E_USER_ERROR);
	  header("Location: $location");
	  header('Cache-Control: no-store, no-cache, must-revalidate, post-check=0, pre-check=0');
	}
	elseif (($hs==true) || ($code==302) || ($code==303))
	{
	  // todo: draw some javascript to redirect
	  // tyler edit: There's your javascript redirect code:
	  print "";
	}
	exit(0);
	}
	$permalink = get_permalink($postid);
	redirect("$permalink",301);
}
else {
	// do nothing
}
?></pre>

<!--adsense-->

  
**  
Another note**, I also removed the CSS stuff from that function that formats how the link to redirect to is displayed. I removed that because I added javascript to the function to do a javascript redirect if the headers have already been sent and PHP&#8217;s redirect() function can&#8217;t be used.

So, the function above should work well for anyone wanting to do some URL redirection. But back to the point of this post. Since my headers haven&#8217;t been sent at the time the function is run, PHP&#8217;s header() function is used to let the user-agent know how to respond. Now, that part is key in keeping my search rankings high, because search engines, or Google at least, pay attention to 301 Permanent Redirect codes. [This topic at the Webmaster World forums describes][3] a bit about why 301 redirects work for Google. [GoogleGuy][4] himself confirmed that the method mentioned there is indeed the best way to do a google-friendly redirect.

So, now that we know we&#8217;re using the best redirection method, we should be set. This is by no means an end all solution to maintaining search rankings after changing a sites permalink structure. And this method would only work if your previous permalink structure was setup like /archives/%postid%/. It could be modified to work for other environments however.

Let me explain the code at the top a little, specifically this piece:

<pre>$uri = $_SERVER[REQUEST_URI];
$uri = explode("/",$uri);
$dir = $uri[1];
$postid = $uri[2];
if ($dir == "archives" && $postid != "") {
  // register and call redirect function here
}</pre>

The first line gets the URI requested by the searcher. After that, the explode function is used to split the URI up based on where slashes (/) occur. So, text before and after the slashes will get put into an array, $uri. Then the different pieces of the URI are put into separate variables, $dir and $postid. Now that we have at very least the post id, we can find the post the searcher was looking for.

The if statement checks to make sure the searcher is coming to the /archives/ page, which is how my permalinks used to be. For example, searching for &#8220;[slackware 11][5]&#8221; returns results for this site, but they URL&#8217;s are pointed at my old permalinks, and that page obviously doesn&#8217;t exist anymore. If the searcher isn&#8217;t coming in to an old archive page, the whole chunk of redirection code gets ignored.

Now for the final and most important piece of code (and probably simplest), fetching the new permalink.

<pre>$permalink = get_permalink($postid);
	redirect("$permalink",301);</pre>

The first line line is a wordpress function that grabs the permalink of a post based on it&#8217;s post id, which we have in the $postid variable from the previous chunk of code. Once the new permalink is obtained, we can pass it through the redirect function from above and all will be well. You can optionally add a status code to the redirect function, as I have for the 301 specific status code.

So, after all that, when a search engine user gets sent to one of my old permalinks, they will be redirected to the new permalink after clicking on the 301 redirect confirmation page. Dirty but it gets the job done, and supposedly will keep Google and other search engines from un-indexing some of my posts.

I think that&#8217;s about it, if you have any questions please feel free to [contact me][6] or leave a comment. I should also mention I [tried this permalink redirection WordPress plugin][7], but it didn&#8217;t work right out of the box and I didn&#8217;t want to take the time to hack that plugin to do what I want. Oh, and before I forget, check out this [case study I did with Zend back in 2000][8]. I somehow came across it today while browsing the web. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2217"
					data-ulike-nonce="6c103084b6"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2217"></button><span class="count-box"></span>
  </div>
</div>

[][9]{.later-button-el}

<div class='what-next'>
  <h2>
    Well, now what?
  </h2>
  
  <div class='hire'>
    <h3>
      Work with Me
    </h3>
    
    <p>
      I'm available for hire and always taking new clients, big and small. Got a project or an idea you'd like to discuss? Startup plan but no developer to make it happen? Just <a href='https://www.longren.io/contact/'>get in touch</a>, I'd love to see if I can help you out!
    </p></p>
  </div>
  
  <div class='hire'>
    <h3>
      Leave some Feedback
    </h3>
    
    <p>
      Got a question or some updated information releavant to this post? Please, <a href='#respond' title='Leave a comment'>leave a comment</a>! The comments are a great way to get help, I read them all and reply to nearly every comment. Let's talk. 😀
    </p></p>
  </div>
  
  <div class='now-what-bottom-ad'>
    <h3>
      Longren.io is proudly hosted by <a href='https://www.digitalocean.com/?refcode=cbf49d0481c8'>DigitalOcean</a>
    </h3>
    
    <p>
      <span class='do_link'><a href='https://www.digitalocean.com/?refcode=cbf49d0481c8' rel='nofollow' target='_blank'><img alt='DigitalOcean' border='0' src='https://i0.wp.com/longren.io/wp-content/uploads/2014/03/digitalocean.png?w=1100&#038;ssl=1' data-recalc-dims="1" /></a></span><br /> <!--

<h3>Need Cloud Monitoring? Try Mist.io!</h3>

<span class='do_link'><a href='http://mist.io/?ref=tyler' rel='nofollow' target='_blank'><img alt='Mist.io' border='0' src='https://i0.wp.com/longren.io/wp-content/uploads/2014/04/mistio.jpg?w=1100&#038;ssl=1' data-recalc-dims="1"></a></span>--></div> </div>

 [1]: http://www.longren.org/2006/08/18/permalink-structure-update/
 [2]: http://edoceo.com/creo/php-redirect.php
 [3]: http://www.webmasterworld.com/forum3/11541.htm
 [4]: http://www.webmasterworld.com/profilev4.cgi?action=view&member=GoogleGuy
 [5]: http://www.google.com/search?q=slackware+11&hl=en&hs=sZI&lr=&client=firefox-a&rls=org.mozilla:en-US:official&start=10&sa=N
 [6]: http://www.longren.org/contact/
 [7]: http://fucoder.com/code/permalink-redirect/
 [8]: http://www.zend.com/zend/cs/tyler.php
 [9]: #