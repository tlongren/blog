---
title: Wicd.net Now Points to Launchpad
author: Tyler Longren
type: post
date: 2013-10-21T05:27:40+00:00
url: /wicd-net-now-points-to-launchpad/
featured_image: /wp-content/uploads/2013/10/wicd_net-e1382332466620.png
dsq_thread_id:
  - 1881424232
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - Internet
  - Linux
  - Open Source
  - Personal

---
Back in July of 2007 I purchased the domain [wicd.net][1], for Adam Blackburn. I chose to do so because Adam&#8217;s [Wicd software][2] was the only thing that would reliably work with the wireless card I had in an rather old laptop. Adam still seems to be maintaining the project, too!

Anyway, wicd.net used to host apt repos and documentation, but now all that is taken care of at [Laundhpad][2]. Since I didn&#8217;t think Adam wanted to continue using the wicd.net domain, I used the domain for a couple things. [Sourceforge][3], and [Launchpad][2], provide most of the resources a project maintainer requires. Using a custom domain for everything just adds time and lots of other headaches that could be avoided. Not to mention the time expense. As a developer, I&#8217;d rather focus on developing (implementing features, bug fixes, etc.) instead of server management, I _do_ happen to enjoy server management, too. Up to a point at least, heh.

The first thing I did with wicd.net was copy all of the original page content and mirror it on a WordPress install. I didn&#8217;t mirror any files, just documentation stuff. I had bold links pointing to the, at the time, [new page at SourceForge][3] (which, has since moved to [Launchpad][2]). That was obviously a bad idea though, as the information was dangerously out-dated.

Next I had it pointed to my [About page, here at longren.org][4], but that was also a bad idea because people actually had to read to find the link to [the new Wicd site][2]. And that sucks.

So, I just setup some [Apache mod_rewrite rules][5] to direct all traffic coming to wicd.net to the current, [official, page at Launchpad][2].

<div class="oembed-gist">
  <noscript>
    View the code on <a href="https://gist.github.com/tlongren/7079037">Gist</a>.
  </noscript>
</div>

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="4765"
					data-ulike-nonce="2c93b2e684"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_4765"></button><span class="count-box"></span>
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

 [1]: http://wicd.net/
 [2]: https://launchpad.net/wicd
 [3]: http://wicd.sourceforge.net/
 [4]: http://www.longren.org/about/
 [5]: https://gist.github.com/tlongren/7079037
 [6]: #