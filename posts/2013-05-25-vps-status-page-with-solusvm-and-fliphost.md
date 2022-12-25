---
title: VPS Status Page with SolusVM and FlipHost
author: Tyler Longren
type: post
date: 2013-05-25T04:07:48+00:00
url: /vps-status-page-with-solusvm-and-fliphost/
featured_image: /wp-content/uploads/2013/05/vps-status-screenshot.png
dsq_thread_id:
  - 1385919089
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - fliphost
  - git
  - heroku
  - Internet
  - Linux
  - PHP

---
I found out that [FlipHost][1] offers access to server stats through an [API developed by SolusVM][2]. It offers all the stuff you&#8217;d want to know about your VPS. Disk usage, RAM usage, bandwidth usage, but I don&#8217;t think it does any cpu load reporting, unfortunately.

I put [together a simple site][3] to quickly tell if all my stuff at FlipHost was online. I could have gone the pinging the VPS IP route, but since there was an API available, I might as well use it. And pinging a host wouldn&#8217;t give all these details.

If you have a VPS from FlipHost, you can generate your API key and API hash from your SolusVM Control Panel, in the &#8220;api&#8221; tab. **If you don&#8217;t use FlipHost**, but your host does use SolusVM, this should work for you too. The **API client URL for FlipHost** is: _https://solus.fliphost.net/api/client_. The SolusVM client API suggests the client URL is run on port 5656, but FlipHost has directed port 80 and 443 there instead.

The site is [available on Github][4], so you can easily make your own status page. I&#8217;ll be adding more to it, as there&#8217;s only really one action being taken currently. As a demo, I&#8217;ve put it up at <http://status.longren.org/>, which is [hosted on Heroku][5]. It also looks nice on mobile devices. Have a look at the screenshots in the gallery at the end of this post.

You should be able to deploy this on [Heroku][6] just like any other app. Just [fork it on Github][4], make a local clone of your forked repo, edit config.php, setup your Heroku git remote, and push to Heroku. You&#8217;ll want to [install the Heroku Toolbelt app][7]. The [Heroku Dev Center][8] is a great resource if you&#8217;re new to Heroku.

For a more detailed explanation on setting this up on Heroku, you&#8217;ll want to read _[How-To: Monitor VPS Status from Heroku][9]_.  
<!--more-->

  
<!-- see gallery_shortcode() in wp-includes/media.php -->

<div id='gallery-12' class='gallery galleryid-4416'>
  <dl class='gallery-item'>
    <dt class='gallery-icon'>
      <a href='https://i2.wp.com/www.longren.io/wp-content/uploads/2013/05/framed_2013-05-31-00.09.29.png?ssl=1'><img width="150" height="150" src="https://i2.wp.com/www.longren.io/wp-content/uploads/2013/05/framed_2013-05-31-00.09.29.png?resize=150%2C150&#038;ssl=1" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" srcset="https://i2.wp.com/www.longren.io/wp-content/uploads/2013/05/framed_2013-05-31-00.09.29.png?resize=150%2C150&ssl=1 150w, https://i2.wp.com/www.longren.io/wp-content/uploads/2013/05/framed_2013-05-31-00.09.29.png?resize=200%2C200&ssl=1 200w, https://i2.wp.com/www.longren.io/wp-content/uploads/2013/05/framed_2013-05-31-00.09.29.png?zoom=2&resize=150%2C150&ssl=1 300w, https://i2.wp.com/www.longren.io/wp-content/uploads/2013/05/framed_2013-05-31-00.09.29.png?zoom=3&resize=150%2C150&ssl=1 450w" sizes="(max-width: 150px) 100vw, 150px" data-recalc-dims="1" /></a>
    </dt>
  </dl>
  
  <dl class='gallery-item'>
    <dt class='gallery-icon'>
      <a href='https://i0.wp.com/www.longren.io/wp-content/uploads/2013/05/framed_2013-05-31-01.04.28.png?ssl=1'><img width="150" height="150" src="https://i0.wp.com/www.longren.io/wp-content/uploads/2013/05/framed_2013-05-31-01.04.28.png?resize=150%2C150&#038;ssl=1" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2013/05/framed_2013-05-31-01.04.28.png?resize=150%2C150&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2013/05/framed_2013-05-31-01.04.28.png?resize=200%2C200&ssl=1 200w, https://i0.wp.com/www.longren.io/wp-content/uploads/2013/05/framed_2013-05-31-01.04.28.png?zoom=2&resize=150%2C150&ssl=1 300w, https://i0.wp.com/www.longren.io/wp-content/uploads/2013/05/framed_2013-05-31-01.04.28.png?zoom=3&resize=150%2C150&ssl=1 450w" sizes="(max-width: 150px) 100vw, 150px" data-recalc-dims="1" /></a>
    </dt>
  </dl>
  
  <dl class='gallery-item'>
    <dt class='gallery-icon'>
      <a href='https://i0.wp.com/www.longren.io/wp-content/uploads/2013/05/vps-status-screenshot.png?ssl=1'><img width="150" height="150" src="https://i0.wp.com/www.longren.io/wp-content/uploads/2013/05/vps-status-screenshot.png?resize=150%2C150&#038;ssl=1" class="attachment-thumbnail size-thumbnail" alt="" loading="lazy" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2013/05/vps-status-screenshot.png?resize=150%2C150&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2013/05/vps-status-screenshot.png?resize=200%2C200&ssl=1 200w, https://i0.wp.com/www.longren.io/wp-content/uploads/2013/05/vps-status-screenshot.png?zoom=2&resize=150%2C150&ssl=1 300w, https://i0.wp.com/www.longren.io/wp-content/uploads/2013/05/vps-status-screenshot.png?zoom=3&resize=150%2C150&ssl=1 450w" sizes="(max-width: 150px) 100vw, 150px" data-recalc-dims="1" /></a>
    </dt>
  </dl>
  
  <br style="clear: both" /> <br style='clear: both;' />
</div>

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="4416"
					data-ulike-nonce="aa4e98372c"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_4416"></button><span class="count-box"></span>
  </div>
</div>

[][10]{.later-button-el}

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

 [1]: http://www.fliphost.net/
 [2]: http://docs.solusvm.com/client_api
 [3]: http://status.longren.org/
 [4]: https://github.com/tlongren/vps-status
 [5]: http://heroku.com
 [6]: http://www.heroku.com/
 [7]: https://toolbelt.heroku.com/
 [8]: https://devcenter.heroku.com/articles/git
 [9]: http://www.longren.org/how-to-monitor-vps-status-from-heroku/
 [10]: #