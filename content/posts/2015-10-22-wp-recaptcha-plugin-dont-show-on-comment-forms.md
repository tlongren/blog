---
title: New WordPress Plugin to Disable ReCaptha on Comment Forms
author: Tyler Longren
type: post
date: 2015-10-22T12:50:52+00:00
draft: true
url: /?p=8206
featured_image: /wp-content/uploads/2015/10/bg-ease-01.png
independent_publisher_primary_category:
  - WordPress
dsq_thread_id:
  - 4247500919
tags:
  - cool
  - how-to
  - Internet
  - Open Source
  - PHP
  - plugins
  - themes
  - tutorials
  - WordPress

---
## WP-Recaptcha Plugin, prevent it from Showing on Comment Forms {.subtitle}

A client of mine started using [Google ReCaptcha][1] recently, but they only wanted it for use on the user registration pages. I decided to use the [WP-ReCaptcha plugin][2]. For those of you unfamiliar with ReCaptcha, here&#8217;s a good explanation from Google:

> reCAPTCHA is a free service that protects your website from spam and abuse. reCAPTCHA uses an advanced risk analysis engine and adaptive CAPTCHAs to keep automated software from engaging in abusive activities on your site. It does this while letting your valid users pass through with ease.
> 
> reCAPTCHA offers more than just spam protection. Every time our CAPTCHAs are solved, that human effort helps digitize text, annotate images, and build machine learning datasets. This in turn helps preserve books, improve maps, and solve hard AI problems.

The screenshot of the plugin options page (below) shows that you can enable or disable ReCaptcha on comments or for the registration form. It&#8217;s a lie. That must have been for an older version, because the current version, 4.1, offers no such options.  
<a href="https://i0.wp.com/longren.io/wp-content/uploads/2015/10/screenshot-1.png?ssl=1" rel="attachment wp-att-8211"><img loading="lazy" src="https://i1.wp.com/longren.io/wp-content/uploads/2015/10/screenshot-1-225x300.png?resize=225%2C300" alt="screenshot-1" width="225" height="300" class="aligncenter size-medium wp-image-8211" srcset="https://i1.wp.com/www.longren.io/wp-content/uploads/2015/10/screenshot-1.png?resize=225%2C300&ssl=1 225w, https://i1.wp.com/www.longren.io/wp-content/uploads/2015/10/screenshot-1.png?resize=113%2C150&ssl=1 113w, https://i1.wp.com/www.longren.io/wp-content/uploads/2015/10/screenshot-1.png?resize=526%2C700&ssl=1 526w, https://i1.wp.com/www.longren.io/wp-content/uploads/2015/10/screenshot-1.png?w=669&ssl=1 669w" sizes="(max-width: 225px) 100vw, 225px" data-recalc-dims="1" /></a>

I came across another user having [the same issue in the WP-Recaptcha forums][3]. After a bit of digging around in the plugin source, I found the _comment_form_ hook. It must be of some use here, right?

Hoping the _comment_form_ hook would do as its name would suggest, along with the code To prevent Google&#8217;s ReCaptcha from displaying on comment forms, simply add this code to the _functions.php_ file for your theme, or to your functionality plugin.

Rather than mess around, I simply re-added the option to disable/enable ReCaptcha on comment forms. The source is avaialble on GitHub and is entirely based on the work of the [WP-reCAPTCHA developers][2]. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="8206"
					data-ulike-nonce="0107f668f7"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_8206"></button><span class="count-box"></span>
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

 [1]: https://www.google.com/recaptcha/intro/index.html
 [2]: https://wordpress.org/plugins/wp-recaptcha/
 [3]: https://wordpress.org/support/topic/turn-off-recaptcha-for-comment-form?replies=4
 [4]: #