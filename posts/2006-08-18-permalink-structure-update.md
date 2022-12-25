---
title: Permalink Structure Update
author: Tyler Longren
type: post
date: 2006-08-18T14:42:26+00:00
url: /permalink-structure-update/
views:
  - 2309
dsq_thread_id:
  - 1708895615
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - blog
  - blogging
  - blogs
  - permalink
  - url
  - website
  - WordPress
  - www

---
I&#8217;ve updated the permalink structure on this blog. What&#8217;s this mean for you? Nothing really, unless you had some pages bookmarked. If you did have some pages at this blog bookmarked, they&#8217;ll no longer load to the right page. My permalinks used to look like this: http://longren.org/archives/2182

Now, they look something like this:  
http://www.longren.org/2006/07/28/the-pc-de-crapifier/

There&#8217;s no real benefit gained from this change, I just like the look of the new permalink structure better. Now, the only problem with making this change is search engines still see the old permalink structure, as expected. So, when someone [searches google for Slackware 11][1], they will see a link to http://www.longren.org/archives/2156.

Well, the /archives/2156 page no longer exists here. However, there is an /archives/ page. I&#8217;ve added a slight bit of intelligence to the /archives/ page. If a user ends up at www.longren.org/archives/2156/, the archives page will try to find the post they&#8217;re really looking for.

Now, this works very well for people coming in from search engines or other blogs that have linked here. Any time the archives page sees a number at the end, /archives/2156, for example, it assumes the number is a postid, which is usually is. So, after that, the PHP code fetches the new URL for the post id and then grabs the post title and provides a link to the new URL.

Here&#8217;s the PHP I used to make this happen:

<pre><?php
$uri = $_SERVER[REQUEST_URI];
$uri = explode("/",$uri);
$postid = $uri[2];
if (strlen($postid) <= "4") {
	$permalink = get_permalink($postid);
	$post = get_post($postid);
	$title = $post->post_title;
	print "

<h3>
  <a href='$permalink'>$title</a>
</h3>

<br />";
}
?></pre>

Not very pretty, I know, but it gets the job done. Oh, and I really like [this Code Autoescape plugin][2]. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2215"
					data-ulike-nonce="2f3fccdfc1"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2215"></button><span class="count-box"></span>
  </div>
</div>

[][3]{.later-button-el}

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

 [1]: http://www.google.ca/search?q=slackware%2011&hl=en&hs=d8t&lr=&safe=off&client=firefox-a&rls=org.mozilla:en-US:official&start=10&sa=N
 [2]: http://priyadi.net/archives/2005/09/27/wordpress-plugin-code-autoescape/
 [3]: #