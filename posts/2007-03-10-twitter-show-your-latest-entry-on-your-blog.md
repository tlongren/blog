---
title: 'Twitter: Show Your Latest Entry On Your Blog'
author: Tyler Longren
type: post
date: 2007-03-10T15:01:56+00:00
url: /twitter-show-your-latest-entry-on-your-blog/
views:
  - 17226
ratings_users:
  - 6
ratings_score:
  - 25
ratings_average:
  - 4.17
dsq_thread_id:
  - 1385934660
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - code
  - howto
  - Internet
  - Noteworthy
  - Personal
  - PHP
  - plugin
  - twitter
  - WordPress
  - wordpress-plugin

---
Want to show your latest entry to [Twitter][1] on your [WordPress][2] blog or website? It&#8217;s really very simple. Don&#8217;t be scared off by the vague instructions for adding a badge at the [Twitter Badge page][3]. The Twitter Badge page has some Flash badges at the very top and some javascript badges immediately below the Flash badges.  
<!--adsense-->

  
We&#8217;re mostly interested in the javascript badges. I don&#8217;t give two shits about Flash and refuse to add something to this site that will cause unnecessary lag just because it&#8217;s &#8220;pretty&#8221;. I&#8217;m a pretty devout follower of the K.I.S.S. philosophy. And besides, all we&#8217;re covering here is how to show your latest Twitter entry, pretty basic. Take a look below to see how I display &#8220;My Latest Twitter&#8221; in my sidebar.

> **1.** Open your themes sidebar.php file (probably in /wp-content/themes/_theme_name_/).
> 
> **2.** Determine where you would like your Recent Twitter Status to appear in your sidebar.
> 
> **3.** Copy the following code and paste it into sidebar.php in the location you chose in step 2.
> 
> <pre>&lt;div class="sb-lasttwitter"&gt;
&lt;h2&gt;&lt;a href="http://twitter.com/&lt;em&gt;yourTwitterUsername&lt;/em&gt;/"&gt;&lt;?php _e(&#39;My Latest Twitter&#39;); ?&gt;&lt;/a&gt;&lt;/h2&gt;
&lt;ul&gt;&lt;li&gt;
### insert javascript for Twitter Badge here ###
&lt;/li&gt;&lt;/ul&gt;
&lt;/div&gt;
</pre>
> 
> **4.** Open your themes style.css file and add a class called sb-lasttwitter. You can expand on the styling for the sb-lasttwitter class all you want. The CSS I use is below, it should work for most people as-is.
> 
> <pre>/*- most recent twitter*/
.sb-lasttwitter ul li {
	list-style-type: none;
	}
</pre>
> 
> **5.** After adding the sb-lasttwitter CSS class, save your style.css file and upload the newly modified file to your website.
> 
> **6.** Login to your [Twitter account][1] and click the &#8220;Badge&#8221; link at the top.
> 
> **7.** Click the first javascript badge, it should automatically select all of the code when you click on it. Copy the selected javascript code to your clipboard (right-click and copy).
> 
> **8.** After you&#8217;ve copied the badge javascript, go back to sidebar.php and find the line that reads: _\### insert javascript for Twitter Badge here ###_. Replace that line with the javascript you copied from step 7.
> 
> **9.** Save sidebar.php and upload it to your website, it goes in the same directory you uploaded style.css to.
> 
> **10.** Done! Visit your blog to (hopefully) see your latest twitter in the sidebar. 

Once you&#8217;re done with that you should see &#8220;My Latest Twitter&#8221; in your sidebar. Immediately below that text you should see your most recent Twitter and how long ago it was entered.

You should also note that the code from step 2 may not work for every WordPress theme, in fact, it probably won&#8217;t. However, you should be able to make a few simple changes to make it fit perfectly with your blog&#8217;s theme. My point is, you may have to modify that code (and the CSS) to make this show properly with the rest of your blog theme.  
<!--adsense-->

  
Please be aware that the **Twitter javascript badge breaks [XHTML 1.0 Transitional validation][4]**. Fortunately, it&#8217;s an easy fix to get pages including the Twitter javascript badge to validate again. Remember, this is the javascript we copied in step 7.

Anyway, to make it pass XHTML 1.0 Transitional validation, have a look at the very last line of the javascript, towards the end of the line, should look similar to this:

<pre>?callback=twitterCallback&count=1"&gt;&lt;/script&gt; 
</pre>

Replace the text above with the following text:

<pre>?callback=twitterCallback&amp;count=1"&gt;&lt;/script&gt;
</pre>

Modifying the last line of the javascript as described above will make your site/blog pass XHTML 1.0 Transitional validation, assuming nothing else in your site is broken. [WDG has some good information][5] on why this change will help your site pass validation.

If you have any problems with this, please let me know! I will try to help people as much as I can, no promises though. If there&#8217;s enough interest, I may end up throwing together a very simple wordpress plugin to do all this automatically. It would seem the only Twitter WordPress plugins currently available [require][6] the [WordPress Widgets plugin][7], which I don&#8217;t use. I just want a simple plugin to include the basic javascript badge without the need for Widgets. If nothing pops up within the next few weeks I&#8217;ll probably get to work on a plugin of my own.

There are two full featured Twitter WordPress plugins currently in development, both should be fantastic. The first plugin is [Twitter Tools][8] from [Alex King][9]. Twitter Tools aims to provide full integration between Twitter and WordPress. The second plugin in development is [Twitt-Twoo][10] from [Dean J. Robinson][11]. Twitt-Twoo isn&#8217;t aiming to be a full integration plugin like Twitter Tools. Twitt-Twoo is much more basic, although I believe it will allow you to post to twitter right from the sidebar of your blog, provided you&#8217;re logged in. I&#8217;m not sure if that functionality will be included in Twitter Tools as well or not. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2313"
					data-ulike-nonce="b501165f7d"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2313"></button><span class="count-box"></span>
  </div>
</div>

[][12]{.later-button-el}

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

 [1]: http://twitter.com/
 [2]: http://www.wordpress.org/
 [3]: http://twitter.com/account/badge
 [4]: http://validator.w3.org/
 [5]: http://www.htmlhelp.com/tools/validator/problems.html#amp
 [6]: http://www.velvet.id.au/twitter-wordpress-sidebar-widget/
 [7]: http://automattic.com/code/widgets/
 [8]: http://alexking.org/blog/2007/03/07/twitter-tools-roadmap
 [9]: http://alexking.org/
 [10]: http://www.deanjrobinson.com/plugin/twitt-twoo/
 [11]: http://www.deanjrobinson.com/
 [12]: #