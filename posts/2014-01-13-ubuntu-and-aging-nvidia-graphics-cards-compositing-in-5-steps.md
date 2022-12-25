---
title: 'Ubuntu and Aging Nvidia Graphics Cards: Compositing in 5 Steps'
author: Tyler Longren
type: post
date: 2014-01-14T05:12:23+00:00
url: /ubuntu-and-aging-nvidia-graphics-cards-compositing-in-5-steps/
featured_image: /wp-content/uploads/2014/01/Screenshot-01132014-104007-PM.png
dsq_thread_id:
  - 2119439497
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - fucked
  - how-to
  - howto
  - Linux
  - Noteworthy
  - Personal
  - tutorials

---
I&#8217;ve got a pretty old Nvidia Quadro FX 1400 video card in an older IBM that I use as my primary workstation at home. It only has 3GB of RAM, about 4TB of storage, and a dual core Intel Pentium 4 CPU at 3.60GHz. It&#8217;s plenty fast for my needs. I typically run [Sublime Text 3][1], a terminal window with a few tabs, and Chrome Beta with many tabs.

I also use Docky, I&#8217;d really like to find a good replacement for it, but that&#8217;s something for another post.

### 1. Install the 304 nvidia driver.

Just fire up Synaptic Package Manager and search for &#8220;nvidia&#8221;. It&#8217;ll list a lot of stuff, but install the **nvidia-304** and **nvidia-304-dev** packages. After installation is done, go to step 2.

### 2. Select the nvidia-304 driver.

Go to &#8220;Settings Manager&#8221;, then click &#8220;Additional Drivers&#8221;. Select the 304 driver, select the one labeled as &#8220;(proprietary, tested)&#8221;. Look at the screenshot for a detailed view.

### 3. Apply the nvidia-304 driver.

Click **Apply**, right below the driver list. Enter your password, and let it do it&#8217;s thing. It may take a while.

### 4. Generate _xorg.conf_.

Do this with &#8216;_sudo nvidia-xconfig_&#8216;. It&#8217;ll write a new file to _/etc/X11/xorg.conf_. It will also make a backup of an existing _xorg.conf_ if there&#8217;s one there to backup.

### 5. Reboot.

That&#8217;s it, you should have compositing working after a reboot.

**Be aware that updates can break all of this.** After applying almost 200 updates, it reverted me back to the nouveau driver. I had to go through these steps again to get back to the nvidia-304 driver.

It&#8217;s possible that step 1 isn&#8217;t necessary. I think the nvidia-304 driver would probably get installed when you do step 2. I didn&#8217;t try, though.

I&#8217;ve often downloaded drivers right from [nvidia.com][2], but was having a terrible time getting them to build this time. Instead, I just went with the nvidia drivers provided by, um, well, whoever provides them, I guess. Using the nvidia-304 driver found in the Ubuntu repositories seems to be working quite well, so I&#8217;ll probably never have to do the manual download from nvidia.com again.

This applies to Ubuntu 13.10 Saucy Salamander, and more specifically, [the Xubuntu flavor][3]. But, it should work on any of the various flavors of Ubuntu.

Did I mess anything up? If so, please leave a comment here, or you can leave a comment on the [Hacker News thread][4]. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5071"
					data-ulike-nonce="425f33854c"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5071"></button><span class="count-box"></span>
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

 [1]: http://www.sublimetext.com/3
 [2]: http://nvidia.com/
 [3]: http://xubuntu.org/news/saucy-salamander-final/
 [4]: https://news.ycombinator.com/item?id=7055513
 [5]: #