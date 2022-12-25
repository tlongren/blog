---
title: Horrible Lag is Gone
author: Tyler Longren
type: post
date: 2005-10-21T13:43:42+00:00
url: /horrible-lag-is-gone/
views:
  - 2011
dsq_thread_id:
  - 1786947571
tags:
  - apache
  - blog
  - blogs
  - firefox
  - flock
  - invite
  - mozilla
  - ning
  - plugin
  - web
  - WordPress
  - www

---
This site had been experiencing horrible lag over the last few days. I sat down lastnight and got it all figured out. First, I thought it must somehow be related to the new apache httpd server I installed, not the case. After determining that it wasn&#8217;t an apache config problem or something, I started into WordPress. The lag didn&#8217;t come from WordPress itself, but a plugin I was using. Said plugin was [wp-shortstat][1].

After disabling wp-shortstat, the page loads much quicker without the lag when loading the end of the page. It&#8217;s almost like my web server would get to the bottom of the page and then just stop sending the rest of the data to the browser. The browser would get to the very end of the page and just stop loading. If I&#8217;d view the rendered HTML in IE or FireFox, the the trailing &#8220;body&#8221; and &#8220;html&#8221; tags would be missing. It&#8217;s all better now though.

I also downloaded [Flock][2] lastnight at home. It&#8217;s pretty interesting, all sorts of feature for blogs and other services like [del.icio.us][3]. Flock is built on FireFox 1.0. And if you&#8217;d like a WordPress.com blog, download flock and you can get one [without an invite][4] (H/T [IO ERROR][5]). 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2050"
					data-ulike-nonce="2675070c32"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2050"></button><span class="count-box"></span>
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

 [1]: http://dev.wp-plugins.org/wiki/wp-shortstat
 [2]: http://www.flock.com/
 [3]: http://del.icio.us/
 [4]: http://www.ioerror.us/2005/10/20/flock-developer-preview-048/
 [5]: http://www.ioerror.us
 [6]: #