---
title: Motorola Defy Camera is Working on Ice Cream Sandwich (Android 4.0)
author: Tyler Longren
type: post
date: 2012-03-01T15:50:13+00:00
url: /motorola-defy-camera-is-working-on-ice-cream-sandwich-android-4-0/
featured_image: /wp-content/uploads/2012/03/6943837997_c5249dc284_b-480x270.jpg
views:
  - 278
dsq_thread_id:
  - 1537753176
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - android
  - defy
  - ice cream sandwich
  - ics
  - Internet
  - motorola
  - Open Source

---
Quarx released a new build for Defy and Defy+ yesterday. I am now running on his Defy+ build because camera in it works with regular Motorola Defy&#8217;s with a red camera lens. 

Now that everyone has a partially working camera, all Defy/Defy+ users should be quite happy.

If you&#8217;ve got a Red lens Defy, and want to run Ice Cream Sandwich and have a working camera, follow the steps below.

First, you&#8217;ll need some files.

  * [CM9 Kernel][1]
  * [Defy+ 20120302 Nightly][2]
  * [Latest Gapps][3]
  * [Battery fix from Auris][4]

[ad]  
<!--more-->

  
Once you have those files, follow the steps below.

  1. Clear data/factory reset.
  2. Flash CM9 kernel.
  3. Flash Defy+ ICS zip.
  4. Flash Gapps.
  5. Flash battery charge fix.
  6. Wipe cache.
  7. Wipe dalvik cache.
  8. Done, reboot.

Some things to keep in mind:

  1. No Hardware Acceleration (HWA).
  2. Video playback is extremely slow (unusable really), probably due to no HWA yet. 
  3. Chrome Beta doesn&#8217;t work, also due to no HWA.

<!-- see gallery_shortcode() in wp-includes/media.php -->

<div id='gallery-10' class='gallery galleryid-3341'>
  <dl class='gallery-item'>
    <dt class='gallery-icon'>
      <a href='https://www.longren.io/motorola-defy-camera-is-working-on-ice-cream-sandwich-android-4-0/6943838119_4a8d64e799_b/'><img width="150" height="150" src="https://i0.wp.com/www.longren.io/wp-content/uploads/2012/03/6943838119_4a8d64e799_b.jpg?resize=150%2C150&#038;ssl=1" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2012/03/6943838119_4a8d64e799_b.jpg?resize=150%2C150&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2012/03/6943838119_4a8d64e799_b.jpg?zoom=2&resize=150%2C150&ssl=1 300w, https://i0.wp.com/www.longren.io/wp-content/uploads/2012/03/6943838119_4a8d64e799_b.jpg?zoom=3&resize=150%2C150&ssl=1 450w" sizes="(max-width: 150px) 100vw, 150px" data-recalc-dims="1" /></a>
    </dt>
  </dl>
  
  <dl class='gallery-item'>
    <dt class='gallery-icon'>
      <a href='https://www.longren.io/motorola-defy-camera-is-working-on-ice-cream-sandwich-android-4-0/6797724622_bb8d764d75_b/'><img width="150" height="150" src="https://i1.wp.com/www.longren.io/wp-content/uploads/2012/03/6797724622_bb8d764d75_b.jpg?resize=150%2C150&#038;ssl=1" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" srcset="https://i1.wp.com/www.longren.io/wp-content/uploads/2012/03/6797724622_bb8d764d75_b.jpg?resize=150%2C150&ssl=1 150w, https://i1.wp.com/www.longren.io/wp-content/uploads/2012/03/6797724622_bb8d764d75_b.jpg?zoom=2&resize=150%2C150&ssl=1 300w, https://i1.wp.com/www.longren.io/wp-content/uploads/2012/03/6797724622_bb8d764d75_b.jpg?zoom=3&resize=150%2C150&ssl=1 450w" sizes="(max-width: 150px) 100vw, 150px" data-recalc-dims="1" /></a>
    </dt>
  </dl>
  
  <dl class='gallery-item'>
    <dt class='gallery-icon'>
      <a href='https://www.longren.io/motorola-defy-camera-is-working-on-ice-cream-sandwich-android-4-0/6943837997_c5249dc284_b/'><img width="150" height="150" src="https://i0.wp.com/www.longren.io/wp-content/uploads/2012/03/6943837997_c5249dc284_b.jpg?resize=150%2C150&#038;ssl=1" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2012/03/6943837997_c5249dc284_b.jpg?resize=150%2C150&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2012/03/6943837997_c5249dc284_b.jpg?zoom=2&resize=150%2C150&ssl=1 300w, https://i0.wp.com/www.longren.io/wp-content/uploads/2012/03/6943837997_c5249dc284_b.jpg?zoom=3&resize=150%2C150&ssl=1 450w" sizes="(max-width: 150px) 100vw, 150px" data-recalc-dims="1" /></a>
    </dt>
  </dl>
  
  <br style="clear: both" /> <br style='clear: both;' />
</div>

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="3341"
					data-ulike-nonce="a28c185d95"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_3341"></button><span class="count-box"></span>
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

 [1]: http://defy.wdscript.fr/kernel/CM9_Kernel-signed.zip
 [2]: http://quarx2k.ru/cm9-nightly-defy+/CM9-ICS-MR1-120302-jordan.zip
 [3]: http://goo-inside.me/gapps/gapps-ics-20120224-signed.zip
 [4]: http://dl.dropbox.com/u/29851821/ICS%20Defy%20Red%20Lense%20Battery%20Fix.zip
 [5]: #