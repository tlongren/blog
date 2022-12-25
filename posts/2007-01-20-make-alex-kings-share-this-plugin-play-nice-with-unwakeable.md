---
title: Make Alex King’s Share This Plugin Play Nice With Unwakeable
author: Tyler Longren
type: post
date: 2007-01-20T20:45:21+00:00
url: /make-alex-kings-share-this-plugin-play-nice-with-unwakeable/
views:
  - 57
dsq_thread_id:
  - 1385931102
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - ajax
  - blog
  - blogging
  - Internet
  - JavaScript
  - Noteworthy
  - Personal
  - PHP
  - Unwakeable
  - WordPress
  - wordpress-2.1
  - wordpress-plugin
  - wordpress-theme

---
<p class="alert">
  <a href="http://www.longren.org/2007/02/19/wordpress-and-prototype/">Fixed.</a> Unwakeable 2.0 will include this fix.
</p>

My [Unwakeable WordPress theme][1] doesn&#8217;t play nicely with [Alex King&#8217;s Share This][2] WordPress plugin. When Share This is being used, the livesearch feature of Unwakeable doesn&#8217;t work in Internet Explorer 6 or 7. I&#8217;m willing to bet [K2][3] has the same issue. I know for a fact that [Redoable][4] had this problem at one point. 

Livesearch breaks because prototype.js gets loaded twice, first by Unwakeable, then again by Share This. Now, Share This uses the prototype.js that will be included in WordPress 2.1, located at wp-includes/js/prototype.js. We use a custom prototype.js file for Unwakeable. The prototype.js file in Unwakeable will still provide all the functionality needed by Share This.

The prototype.js included in Unwakeable is located at wp-content/themes/unwakeable-1.2/js/prototype.js.php. It has a .php extension because there&#8217;s some PHP code at the top that needs processed before doing anything else. The PHP code tells the browser to cache the prototype.js file, it also sends correct content-type headers so the browser knows it&#8217;s dealing with a javascript file after all is said and done.

I&#8217;ve spent a few days thinking of possible solutions that could be implemented from within Unwakeable. That&#8217;s not possible though, unfortunately. Well, it is possible, but would require filtering all the HTML output by WordPress before it&#8217;s sent to the browser so we could strip out the prototype.js included by Share This. Doing something like that would probably result in a fairly dramatic decrease in performance, so it&#8217;s not an option.

Fortunately, it&#8217;s extremely easy to modify Share This to not load prototype.js. Here&#8217;s what you need to do:

  1. Open wp-content/plugins/share-this/share-this.php
  2. Go to line 352: 
    <pre></pre>

  3. Delete all of line 352 (code above) and you should be left with this on line 351 to line 354 
    <pre>print('



<link rel="stylesheet" type="text/css" href="'.$url.'?akst_action=css" />
');
</pre>

  4. Save share-this.php and upload it to wp-content/plugins/share-this/

That&#8217;s all there is to do to stop Share This from loading prototype.js. It sorta sucks having to ignore the prototype.js that&#8217;s already included with WordPress 2.1. I will probably start working on making Unwakeable work with the prototype.js included in WordPress 2.1.

Does anyone know if it&#8217;s possible to determine if a javascript file has been loaded, from within javascript? I ask because I think Share This will still load a second prototype.js, even if I make Unwakeable work with prototype.js from WordPress 2.1 (the one used by Share This already).

I imagine Alex will come up with a method to determine if prototype.js has already been loaded. Unless javascript won&#8217;t allow identical .js files to be loaded, in which case determining if prototype.js has already been loaded would be pointless. If that&#8217;s the case then I should be good simply making Unwakeable work with prototype.js from WordPress 2.1.

Sorry for the scattered thoughts, this has really been bugging me lately. Anyway, you should be able to make your livesearch work with Share This in Internet Explorer now. This probably applies to most [K2 based WordPress themes][5], but I&#8217;m not sure. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2301"
					data-ulike-nonce="94e4389519"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2301"></button><span class="count-box"></span>
  </div>
</div>

[][6]{.later-button-el}

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

 [1]: http://www.longren.org/unwakeable/
 [2]: http://alexking.org/projects/wordpress/
 [3]: http://www.getk2.com/
 [4]: http://deanjrobinson.com/wordpress/redoable
 [5]: http://k2.stikipad.com/docs/show/K2+Styles+and+Mods
 [6]: #