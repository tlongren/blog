---
title: Flash TWRP .img File From Ubuntu Using Fastboot
author: Tyler Longren
type: post
date: 2014-03-11T03:33:43+00:00
url: /flash-twrp-img-file-from-ubuntu-using-fastboot/
featured_image: /wp-content/uploads/2014/03/twrp.png
dsq_thread_id:
  - 2405527533
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - adb
  - android
  - fastboot
  - Internet
  - Linux
  - nexus
  - nexus4
  - Open Source
  - opensource
  - ubuntu

---
 

I use [TWRP (TeamWin Recovery Project)][1] on my Nexus 4. Back in the day (read: 3 years ago) I used [ClockworkMod Recovery][2], on my Moto Defy, but have since switched to TWRP. I believe there were some licensing issues that drove a lot of people away from CWM. In any case, you&#8217;ll want to install `adb` and `fastboot` before proceeding.

From an Ubuntu distribution (Xubuntu in my case):

<pre class="wp-block-preformatted">sudo apt-get install android-tools-adb android-tools-fastboot</pre>

After adb and fastboot have been installed, boot your Nexus 4 into fastboot mode. Just switch your Nexus 4 off, then turn it back on while holding the volume down button. Keep holding the down button until you see a menu (usually with an Android guy somewhere on the screen). Entering fastboot mode may be different for your device, check the [TWRP site][1], they have instructions for a lot of different devices.

Now, make sure your PC sees your device in fastboot mode. In a terminal window, run `fastboot devices`. If nothing is printed to the terminal, something is wrong, you probably don&#8217;t have fastboot enabled. If you did see some output, you should be good to go.

Download the latest recovery `.img` file [from the TWRP site][3]. Current version as of this post is 2.7.0.0. To flash it using `fastboot`, do this in a terminal:

<pre class="wp-block-preformatted">fastboot flash recovery openrecovery-twrp-2.7.0.0-mako.img</pre>

If everything goes well, you should see something similar to this:

<blockquote class="wp-block-quote">
  <p>
    sending &#8216;recovery&#8217; (8130 KB)&#8230;<br />OKAY [ 0.510s]<br />writing &#8216;recovery&#8217;&#8230;<br />OKAY [ 0.476s]<br />finished. total time: 0.987s
  </p>
</blockquote>

If you see something other than `OKAY` messages, something is probably wrong, and I have no idea what. If you do see the `OKAY` messages, you can either reboot your phone to Android or go to recovery which will take you to TWRP. With TWRP you can make a nandroid backup, flash new roms, flash new gapps, and all kinds of other things.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="6073"
					data-ulike-nonce="9bb14f0c10"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_6073"></button><span class="count-box">3+</span>
  </div>
</div>

[][4]{.later-button-el}

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
    </p>
  </div>
  
  <div class='hire'>
    <h3>
      Leave some Feedback
    </h3>
    
    <p>
      Got a question or some updated information releavant to this post? Please, <a href='#respond' title='Leave a comment'>leave a comment</a>! The comments are a great way to get help, I read them all and reply to nearly every comment. Let's talk. 😀
    </p>
  </div>
  
  <div class='now-what-bottom-ad'>
    <h3>
      Longren.io is proudly hosted by <a href='https://www.digitalocean.com/?refcode=cbf49d0481c8'>DigitalOcean</a>
    </h3>
    
    <span class='do_link'><a href='https://www.digitalocean.com/?refcode=cbf49d0481c8' rel='nofollow' target='_blank'><img alt='DigitalOcean' border='0' src='https://i0.wp.com/longren.io/wp-content/uploads/2014/03/digitalocean.png?w=1100&#038;ssl=1' data-recalc-dims="1" /></a></span> <!--<h3>Need Cloud Monitoring? Try Mist.io!</h3><span class='do_link'><a href='http://mist.io/?ref=tyler' rel='nofollow' target='_blank'><img alt='Mist.io' border='0' src='https://i0.wp.com/longren.io/wp-content/uploads/2014/04/mistio.jpg?w=1100&#038;ssl=1' data-recalc-dims="1"></a></span>-->
  </div>
</div>

 [1]: http://teamw.in/project/twrp2
 [2]: http://forum.xda-developers.com/wiki/ClockworkMod_Recovery
 [3]: http://techerrata.com/browse/twrp2/mako
 [4]: #