---
title: 'WordPress Plugin: Thumbnail Viewer 1.0'
author: Tyler Longren
type: post
date: 2007-01-29T15:49:43+00:00
url: /wordpress-plugin-thumbnail-viewer-10/
ratings_users:
  - 6
ratings_score:
  - 29
ratings_average:
  - 4.83
views:
  - 15534
dsq_thread_id:
  - 1385918830
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - Internet
  - Noteworthy
  - Personal
  - PHP
  - WordPress

---
<p class="download">
  <a href="http://www.longren.org/wordpress/thumbnail-viewer/">1.0 is old, go get the newest.</a>
</p>

**Thumbnail Viewer** is my first WordPress plugin to be released to the public. I used the [WordPress Lightbox 2 plugin][1] as a starting point and implemented CSS and Javascript from the [Image Thumbnail Viewer from Dynamic Drive][2]. There&#8217;s [another WordPress plugin][3] based on the same code from Dynamic Drive, but it doesn&#8217;t have a quicktag to automatically add the code to your posts/pages. The &#8220;loading&#8221; image and text also seems to be broken in that other plugin.

The **Thumbnail Viewer plugin** is simply used to overlay images on a page, similar to [Lightbox JS][4]. Click on the images below to see the **Thumbnail Viewer plugin** in action.  
<!--more-->

  
<a href="https://i0.wp.com/www.longren.org/images/corn.jpg" rel="thumbnail" title="Some Corn"><img loading="lazy" src="https://i1.wp.com/www.longren.org/images/cornThumbnail.jpg?resize=129%2C96" width="129" height="96" alt="Some Corn" data-recalc-dims="1" /></a><a href="https://i1.wp.com/www.longren.org/images/crackerJacks.jpg" rel="thumbnail" title="Some Cracker Jacks!"><img loading="lazy" src="https://i0.wp.com/www.longren.org/images/crackerJacksThumbnail.jpg?resize=98%2C123" width="98" height="123" alt="Some Cracker Jacks" data-recalc-dims="1" /></a><a href="https://i1.wp.com/www.longren.org/images/peas.jpg" rel="thumbnail" title="Some Peas In A Pod"><img loading="lazy" src="https://i2.wp.com/www.longren.org/images/peasThumbnail.jpg?resize=145%2C96" width="145" height="96" alt="Some Peas" data-recalc-dims="1" /></a>

Here&#8217;s a description of the Image Thumbnail Viewer from Dynamic Drive, the code this plugin is based on:

> Image Thumbnail Viewer is a compact, unobtrusive image viewer that can be applied to any link on the page to load the desired image inside a sleek interface based on the link&#8217;s &#8220;href&#8221; value. Simply give the link in question- be it a text link or image thumbnail link- a rel attribute of &#8220;thumbnail&#8221;, and you&#8217;re done.
> 
> This script will center the enlarged image on the page and optionally display a text description based on the activating link&#8217;s &#8220;title&#8221; attribute. A fading effect can be turned on/off to bring the final image into view.

<p class="download">
  <a href="http://www.longren.org/wordpress/thumbnail-viewer/">1.0 is old, go get the newest.</a>
</p>

### Installation

  1. Extract _**wp-thumbnailviewer**_ folder from .zip to _wp-contents/plugins/_.
  2. Go to Plugins in WordPress dashboard and activate _**Thumbnail Viewer**_.
  3. That&#8217;s it! Write a new post to use the quicktag button or simply add rel=thumbnail to any link tag.

<p class="information">
  Functionality in IE7 is broken (sometimes) in 1.0. The div to display the full image works in some IE7 installs but doesn&#8217;t work in others. Will be fixed for 1.1.
</p>

I will be creating a page dedicated to this plugin in the near future, it will house all information related to this plugin. Please, give it a try and let me know how it works out for you. Any feedback is always appreciated. If you decide to use this plugin and have any questions or problems, please leave a comment. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2304"
					data-ulike-nonce="a25aeca382"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2304"></button><span class="count-box"></span>
  </div>
</div>

[][5]{.later-button-el}

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

 [1]: http://zeo.unic.net.my/notes/lightbox-js-version-20/
 [2]: http://www.dynamicdrive.com/dynamicindex4/thumbnail.htm
 [3]: http://www.planeta.toliman.pl/?p=130
 [4]: http://www.huddletogether.com/projects/lightbox/
 [5]: #