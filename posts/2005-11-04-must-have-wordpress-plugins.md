---
title: Must-Have WordPress Plugins
author: Tyler Longren
type: post
date: 2005-11-05T01:45:53+00:00
url: /must-have-wordpress-plugins/
views:
  - 1929
dsq_thread_id:
  - 1385915889
tags:
  - blog
  - blogs
  - movable-type
  - movabletype
  - PHP
  - plugin
  - plugins
  - trackback
  - US
  - WordPress
  - wordpress-plugin
  - wp
  - www

---
**First**, I&#8217;ve got [**WP-Cache 2.0**][1], my favorite of the bunch. I&#8217;ll just let the developer describe what WP-Cache does:

> WP-Cache is an extremely efficient WordPress page caching system to make your site much faster and responsive. It works by caching Worpress pages and storing them in a static file for serving future requests directly from the file rather than loading and compiling the whole PHP code and then building the page from the database. WP-Cache allows to serve hundred of times more pages per second, and to reduce the response time from several tenths of seconds to less than a millisecond.
> 
> WP-Cache started from the “Staticize Reloaded” by matt and billzeller. Most of their recommendations also apply to WP-Cache. Current version, WP-Cache2, is a huge improvement over previous versions of WP-Cache.

<!--adsense-->

  
It does exactly that, nothing more, nothing less. The administration interface is very nice, showing what pages are currently cached and the age of the cached page. It features a cache expiration setting, so a cached page will expire after a given number of seconds. Next time the expired page is hit, a new version will be cached. It also includes the ability to exclude certain pages from being cached. That way, when there&#8217;s any new content posted (new post or a comment), the new page content will be cached, so people never really see an out-of-date page.

Granted, there&#8217;s no noticible speed increase when loading some page, only due to the fact those pages serve so quickly without the cache. It does help with the main page, without a doubt. Before I started using WP-Cache, my database would do roughly 4 queries a second, on average. Now it&#8217;s never averaging more than 2 queries per second.

The **second** plugin is [**IPAT**][2] (Inline Pingbacks And Trackbacks), from [Slobokan][3]. I [wrote about this one before][4], but it deserves to be included here too. At the time, IPAT was the only option as the inline trackback plugin from [Kimberly Emerson][5] was giving a 404 error when trying to download. Seems Kimberly lost the old code, but since then she&#8217;s [written a new version][6] which seems to be exactly like IPAT. IPAT was built on her original inline trackback code.

I&#8217;ll continue using IPAT simply because I&#8217;ve made a few adjustments to it for my own purposes, very minor adjustments at that.  
<!--adsense-->

  
The **third** and final WordPress plugin is &#8220;[**Post Moderation**][7]&#8220;. Although I&#8217;m not using this plugin, I have played around with it quite a bit. I really have no use for it as I&#8217;m the only author at this site (anyone wanna change that, let me know). The post moderation plugin allows multiple authors on your site and lets you maintain full editorial control. Isn&#8217;t that why so many people use MovableType instead of WordPress? Seems silly to buy a software package when there&#8217;s a WordPress plugin that accomplishes basically the same thing. Maybe MovableType has more desireable features than that, but I&#8217;ve seen many people say their reasons for staying with MovableType is to allow multiple authors. This plugin isn&#8217;t even required to have multiple authors in WordPress, it just allows you to keep editorial control over everything that&#8217;s published.

Might be something for you team bloggers to check out. Hopefully you&#8217;ll find one of the three plugins above somewhat useful. I know lots of WordPress people would enjoy inline trackback ability. Probably not so many people would get much use out of WP-Cache, but it sure speeds load times if you&#8217;ve got a lot of content on your main page, or any page for that matter.

Linked for _attention_ at [Outside The Beltway][8], [NIF][9], [Mudville Gazette][10], [basil&#8217;s blog][11], [Iowa Voice][12], and [Common Folk using Common Sense][13]. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2073"
					data-ulike-nonce="ec4f5f0c02"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2073"></button><span class="count-box"></span>
  </div>
</div>

[][14]{.later-button-el}

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

 [1]: http://mnm.uib.es/gallir/wp-cache-2/
 [2]: http://www.slobokan.com/archives/2005/07/01/my-first-plugin-ipat/
 [3]: http://www.slobokan.com/
 [4]: http://www.longren.org/archives/2055
 [5]: http://simplykimberly.com/
 [6]: http://simplykimberly.com/archives/2005/11/03/wp-plugin-inline-trackbacks-20/
 [7]: http://www.blueeye.us/wordpress/2005/02/17/post-moderation-10-stable/
 [8]: http://www.outsidethebeltway.com/archives/12565
 [9]: http://trejrc0.blogspot.com/2005/11/insert-comment-here.html
 [10]: http://www.mudvillegazette.com/archives/003768.html
 [11]: http://www.basilsblog.net/index.php/2005/11/covered-dish-supper-11-4-2005/
 [12]: http://www.iowavoice.com/index.php?/archives/969-Trackback-Festival.html
 [13]: http://commonfolkcommonsense.blogspot.com/2005/11/now-how-do-you-work-one-of-these.html
 [14]: #