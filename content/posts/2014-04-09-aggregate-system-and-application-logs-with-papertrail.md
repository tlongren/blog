---
title: Aggregate System and Application Logs with Papertrail
author: Tyler Longren
type: post
date: 2014-04-09T14:36:22+00:00
url: /aggregate-system-and-application-logs-with-papertrail/
featured_image: /wp-content/uploads/2014/04/papertrail-e1396931847574.png
full_width_featured_image:
  - 1
dsq_thread_id:
  - 2598220179
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
independent_publisher_primary_category:
  - Services
tags:
  - hosting
  - Internet
  - Linux
  - papertrail
  - Personal
  - saas
  - Security
  - services
  - tools
  - tutorials

---
## Frustration-free log management {.subtitle}

I&#8217;ve been using [Papertrail][1] for a few months now, and absolutely love it. Being able to search logs across all my servers at once is crazy nice.

I can even get alerts when someone logs in via SSH, which, by itself, has made [Papertrail][1] well worth it.

A non-production server was compromised, due to a since-rectified configuration issue. Papertrail notified me almost immediately, allowing for immediate action to be taken.

There&#8217;s a variety of pricing plans, and there&#8217;s even a free for life plan, which includes plenty of features for most folks. I&#8217;m currently on the free plan, but plan on upgrading soon. Adding more servers and will need the extra space at Papertrail.

<div id="polls-26" class="wp-polls">
</div>

<div id="polls-26-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

In addition to collecting logs from your servers, you can also send logs from your applications. Got a PHP application that&#8217;s erroring out for some reason? You can send that error to Papertrail for later investigation.

Same deal with Apache logs, MySQL logs, and pretty much every other piece of software that generates logs.

Not many limits on what you can configure Papertrail to do for you. It&#8217;s very powerful.

[I suggest you give it a try][1]. Installation is super easy, especially if you&#8217;re using `rsyslog`. Below is a screenshot of their installation instructions. Doesn&#8217;t get much easier than that.  
[<img loading="lazy" src="https://i1.wp.com/longren.io/wp-content/uploads/2014/04/papertrail-install.png?resize=550%2C607" alt="papertrail-install" width="550" height="607" class="aligncenter size-full wp-image-6380" srcset="https://i2.wp.com/www.longren.io/wp-content/uploads/2014/04/papertrail-install.png?w=550&ssl=1 550w, https://i2.wp.com/www.longren.io/wp-content/uploads/2014/04/papertrail-install.png?resize=135%2C150&ssl=1 135w, https://i2.wp.com/www.longren.io/wp-content/uploads/2014/04/papertrail-install.png?resize=271%2C300&ssl=1 271w" sizes="(max-width: 550px) 100vw, 550px" data-recalc-dims="1" />][2] 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="6376"
					data-ulike-nonce="0c6daea9c0"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_6376"></button><span class="count-box"></span>
  </div>
</div>

[][3]{.later-button-el}

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

 [1]: https://papertrailapp.com/?thank=33d541
 [2]: https://i1.wp.com/longren.io/wp-content/uploads/2014/04/papertrail-install.png
 [3]: #