---
title: Simple Server Monitoring with Ping.gg
author: Tyler Longren
type: post
date: 2014-12-29T04:09:28+00:00
url: /simple-server-monitoring-with-ping-gg/
featured_image: /wp-content/uploads/2014/12/ping.gg_.png
independent_publisher_primary_category:
  - Services
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
dsq_thread_id:
  - 3366035803
tags:
  - cool
  - GitHub
  - hosting
  - Internet
  - monitoring
  - ping.gg
  - services
  - tools
  - uptime

---
 

## It really is the world&#8217;s most simple server monitoring service

Best of all, [Ping.gg][1] is currently free! Ping.gg will ping your server constantly, with an interval of 10 seconds. 

Victor, the ping.gg creator, will be releasing all the Go code on GitHub eventually, but will keep the UI/PHP pieces to himself. It sounds like HTTP response checking is also in the works:

<blockquote class="wp-block-quote">
  <p>
    There is a ping daemon (Go app) that is listening for a couple of redis pub/sub channels for hosts to start and stop pinging. Each host is handled by a different goroutine. When something goes up or down, it publishes the host in another 2 redis pub/sub channels.
  </p>
  
  <p>
    This is what I&#8217;ll release as open source, before I do I&#8217;d like to refactor it so it&#8217;s not tightly couple with redis, but rather have an interface there, so it&#8217;s easy to change the redis pub/sub interface with, for example, HTTP calls.
  </p>
</blockquote>

### Monitor a Site with Ping.gg

To monitor a site (my.example.com), issue this command: 

<pre class="wp-block-preformatted">curl ping.gg/me@example.org/my.example.com</pre>

I&#8217;ll let Victor explain how it works:

<blockquote class="wp-block-quote">
  <p>
    After you provide a hostname or IP and your email address, you&#8217;ll be sent an email with 3 generated URLs that you can to click to start, stop and delete your tracking. Every time you server goes down or back online you will receive a notification, which will also include the control URLs. BTW, check your spam folder&#8230; you know the drill.
  </p>
</blockquote>

<div class="wp-block-image">
  <figure class="aligncenter"><a href="https://i1.wp.com/longren.io/wp-content/uploads/2014/12/ping.gg-down-email.png?ssl=1"><img loading="lazy" width="1024" height="438" src="https://i2.wp.com/longren.io/wp-content/uploads/2014/12/ping.gg-down-email-1024x438.png?resize=1024%2C438" alt="ping.gg-down-email" class="wp-image-7860" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/12/ping.gg-down-email.png?resize=1024%2C438&ssl=1 1024w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/12/ping.gg-down-email.png?resize=150%2C64&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/12/ping.gg-down-email.png?resize=300%2C128&ssl=1 300w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/12/ping.gg-down-email.png?resize=700%2C299&ssl=1 700w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/12/ping.gg-down-email.png?w=1212&ssl=1 1212w" sizes="(max-width: 1024px) 100vw, 1024px" data-recalc-dims="1" /></a></figure>
</div>

Every time `my.example.com` is unreachable, you&#8217;ll receive an email at `me@example.org`. An example email is below.  


### That&#8217;s It

Issuing that `curl` command is all you need to do. You&#8217;ll receive an email after adding a site to monitor asking you to active the monitoring. There&#8217;s also a link in that email so you can stop or pause monitoring of a site if you wish.

Ping.gg allows 10 sites to be monitored per email address. Ping.gg considers your server/site to be down when it fails to answer 6 pings in a row.

Hoping that Victor builds this into a full fledged service with account dashboards and all, just because it&#8217;s sooo simple. The Terms of Service possibly indicate that a professional service may be available at some point:

<blockquote class="wp-block-quote">
  <p>
    As previously stated, this is not a professional service (not now at least) so by using this service you agree to the following:
  </p>
</blockquote>

  1. You use this service at your own risk.
  2. There is no warranty that the service will work properly or at all.
  3. Your alerts might be terminated without notice.
  4. The service can stop operating anytime without notice.

Go ahead and [give Ping.gg a try][1], it&#8217;s been very reliable for me and I&#8217;ve had no issues with it. Keep the Terms of Service in mind, however.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7856"
					data-ulike-nonce="f833bb9582"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7856"></button><span class="count-box"></span>
  </div>
</div>

[][2]{.later-button-el}

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

 [1]: https://ping.gg/
 [2]: #