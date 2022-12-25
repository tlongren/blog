---
title: New PHP Breaks WP-ShortStat
author: Tyler Longren
type: post
date: 2005-09-07T21:24:08+00:00
url: /new-php-breaks-shortstat/
views:
  - 2033
dsq_thread_id:
  - 1385926070
tags:
  - asp
  - microsoft
  - mysql
  - PHP
  - plugin
  - WordPress

---
So, I just upgraded this server to [PHP 5.0.5][1] with the [0.4.2 hardening patch][2]. All seemed to be going well until I tried to look at my WordPress ShortStat page. It no longer loads from within my WordPress dashboard. [WP-ShortStat][3] is a plugin for WordPress that&#8217;s based on [ShortStat by Shaun Inman][4]. When I say ShortStat I mean the WordPress plugin, WP-ShortStat.

The table that stores ShortStat data has roughly 150,000 records. ShortStat is still logging statistics to the database table, it&#8217;s method for displaying the data within the WordPress dashboard is just broken. Very annoying as I very much enjoy watching the ShortStat page for this blog. I&#8217;ll either fix it tonight or find some other method for tracking visitor stats.

The end user shouldn&#8217;t notice anything different in the functionality of the site.

**UPDATE:** After commenting out the following piece of code on line 605 of wp-shortstat.php everything works fine.

<pre>gmdate("g:i a j M Y",$wpss->getFirstHit()+(((gmdate('I'))?
($wpss->$tz_offset+1):$wpss->$tz_offset)*3600));</pre>

Take not that if you remove the code listed above from line 605 of wp-shortstat.php, the date will no longer display at the top of the &#8220;Hits/Uniques&#8221; section. The date displayed there is the very first date WP-ShortStat started logging. So that&#8217;s the only adverse effect you should notice from removing that line.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2001"
					data-ulike-nonce="f7850862dc"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2001"></button><span class="count-box"></span>
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

 [1]: http://www.php.net/ChangeLog-5.php#5.0.5
 [2]: http://www.hardened-php.net/hardening-patch_v042_released.68.html
 [3]: http://dev.wp-plugins.org/wiki/wp-shortstat
 [4]: http://shortstat.shauninman.com/
 [5]: #