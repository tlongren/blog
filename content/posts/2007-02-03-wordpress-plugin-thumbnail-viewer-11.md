---
title: 'WordPress Plugin: Thumbnail Viewer 1.1'
author: Tyler Longren
type: post
date: 2007-02-04T01:40:55+00:00
url: /wordpress-plugin-thumbnail-viewer-11/
ratings_users:
  - 20
ratings_score:
  - 72
ratings_average:
  - 3.6
views:
  - 41128
DiggUrl:
  - http://digg.com/software/Thumbnail_Viewer_WordPress_Plugin
dsq_thread_id:
  - 1385923508
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - Internet
  - Noteworthy
  - Personal
  - PHP
  - thumbnail-viewer
  - WordPress
  - wordpress-plugin
  - wordpress-plugins
  - wordpress-thumbnail-viewer

---
<p class="download">
  <a href="http://www.longren.org/wordpress/thumbnail-viewer/">1.1 is now old, go get the newest.</a>
</p>

I&#8217;ve released version 1.1 of my **Thumbnail Viewer plugin**, which still needs an official homepage. This release was prompted by a problem with showing the quicktag when authoring a new post or page. The quicktag wasn&#8217;t showing on WordPress 2.1 installations. So, as a result, WordPress 2.0.x is no longer supported by the **Thumbnail Viewer plugin**. If you want to use this plugin you&#8217;ll need WordPress 2.1 or later. Really, the plugin should still work with WordPress 2.0.x, however the quicktag won&#8217;t be available when writing a new post.  
<!--adsense-->

  
The issues in Internet Explorer 7 [I spoke about earlier][1] haven&#8217;t been resolved, quite. I&#8217;d say the plugin works fine in 98% or more of all Internet Explorer 7 installations. I&#8217;ve only had problems on one installation of IE7. I&#8217;m pretty sure this problem isn&#8217;t even directly related to this plugin. I say that because [the demo page for the code][2] this plugin is based on won&#8217;t work either in that same IE7 install. So, it&#8217;s apparently a problem in the javascript this plugin is based on. I guess as of right now, I&#8217;m considering the div display problem in IE7 to be out of my control.

Anyway, click the images below for a demo.  
<a href="https://i0.wp.com/www.longren.org/images/corn.jpg" rel="thumbnail" title="Some Corn"><img loading="lazy" src="https://i1.wp.com/www.longren.org/images/cornThumbnail.jpg?resize=129%2C96" width="129" height="96" alt="Some Corn" data-recalc-dims="1" /></a><a href="https://i1.wp.com/www.longren.org/images/crackerJacks.jpg" rel="thumbnail" title="Some Cracker Jacks!"><img loading="lazy" src="https://i0.wp.com/www.longren.org/images/crackerJacksThumbnail.jpg?resize=98%2C123" width="98" height="123" alt="Some Cracker Jacks" data-recalc-dims="1" /></a><a href="https://i1.wp.com/www.longren.org/images/peas.jpg" rel="thumbnail" title="Some Peas In A Pod"><img loading="lazy" src="https://i2.wp.com/www.longren.org/images/peasThumbnail.jpg?resize=145%2C96" width="145" height="96" alt="Some Peas" data-recalc-dims="1" /></a>

The above example was achieved with the following HTML:

<pre><a href="https://i0.wp.com/www.longren.org/images/corn.jpg" rel="thumbnail" title="Some Corn"><img loading="lazy" src="https://i1.wp.com/www.longren.org/images/cornThumbnail.jpg?resize=129%2C96" width="129" height="96" alt="Some Corn" data-recalc-dims="1" /></a>
<a href="https://i1.wp.com/www.longren.org/images/crackerJacks.jpg" rel="thumbnail" title="Some Cracker Jacks!"><img loading="lazy" src="https://i0.wp.com/www.longren.org/images/crackerJacksThumbnail.jpg?resize=98%2C123" width="98" height="123" alt="Some Cracker Jacks" data-recalc-dims="1" /></a>
<a href="https://i1.wp.com/www.longren.org/images/peas.jpg" rel="thumbnail" title="Some Peas In A Pod"><img loading="lazy" src="https://i2.wp.com/www.longren.org/images/peasThumbnail.jpg?resize=145%2C96" width="145" height="96" alt="Some Peas" data-recalc-dims="1" /></a></pre>

<p class="download">
  <a href="http://www.longren.org/wordpress/thumbnail-viewer/">1.1 is now old, go get the newest.</a>
</p>

### Installation

  1. Extract _**wp-thumbnailviewer**_ folder from .zip to _wp-contents/plugins/_.
  2. Go to Plugins in WordPress dashboard and activate _**Thumbnail Viewer**_.
  3. That&#8217;s it! Write a new post to use the quicktag button or simply add rel=thumbnail to any link tag.

### Upgrading

  1. Simply overwrite everything in _wp-contents/plugins/wp-thumbnailviewer/_ with everything in the _**wp-thumbnailviewer**_ folder from the zip file.
  2. That&#8217;s it! You should now be using the latest Thumbnail Viewer WordPress plugin.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2308"
					data-ulike-nonce="b4f3350dd0"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2308"></button><span class="count-box"></span>
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

 [1]: http://www.longren.org/2007/01/29/wordpress-plugin-thumbnail-viewer-10/
 [2]: http://www.dynamicdrive.com/dynamicindex4/thumbnail.htm
 [3]: #