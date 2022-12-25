---
title: VLC Media Player for Android on Motorola Defy and Defy+
author: Tyler Longren
type: post
date: 2011-09-27T14:53:03+00:00
url: /vlc-media-player-for-android-on-motorola-defy-and-defy/
featured_image: /wp-content/uploads/2011/09/vlc-480x270.png
views:
  - 428
dsq_thread_id:
  - 1385932464
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - android
  - Internet

---
[Austen Dicken][1] has been working on [VLC Media Player for Android devices][2]. He stresses that it&#8217;s not stable and is still in the pre-alpha stages. I installed it the other day and haven&#8217;t noticed any real problems with it.

There&#8217;s two builds of VLC for Android available for download on Austen&#8217;s site. There&#8217;s a NEON version and a NONEON version. The NEON build is for devices that have processors that support NEON floating-point extensions.  
[ad]  
If you&#8217;ve got a Motorola Defy or Motorola Defy+, you&#8217;ll want the NEON build. The processors in both phones are similar and both support NEON floating-point extensions.  
<!--more-->

  
If you don&#8217;t have one of those devices, it&#8217;s easy to find out what build you need. Just open /proc/cpuinfo on your phone and look for NEON in the Features line. If NEON is listed there, you want the NEON build. If NEON isn&#8217;t listed, get the NONEON build. You may need to root your phone before you can access /proc/. I use  
[Root Explorer][3] for browsing my root filesystem.

The contents of your /proc/cpuinfo file will look similar to this:

<pre>Processor	: ARMv7 Processor rev 2 (v7l)
BogoMIPS	: 1198.44
Features	: swp half thumb fastmult vfp edsp neon vfpv3 
CPU implementer	: 0x41
CPU architecture: 7
CPU variant	: 0x3
CPU part	: 0xc08
CPU revision	: 2

Hardware	: mapphone_UMTS
Revision	: 0000
Serial		: 0000000000000000
CPU Tier	: 10
</pre>

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="3059"
					data-ulike-nonce="548c8eb9ff"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_3059"></button><span class="count-box"></span>
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

 [1]: http://cvpcs.org/info/about
 [2]: http://cvpcs.org/blog/2011-09-18/videolan_for_android_pre-alpha
 [3]: https://market.android.com/details?id=com.speedsoftware.rootexplorer&feature=search_result
 [4]: #