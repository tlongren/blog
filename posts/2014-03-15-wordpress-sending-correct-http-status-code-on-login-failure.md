---
title: 'WordPress: Sending Correct HTTP Status Code on Login Failure'
author: Tyler Longren
type: post
date: 2014-03-15T05:20:12+00:00
url: /wordpress-sending-correct-http-status-code-on-login-failure/
featured_image: /wp-content/uploads/2014/03/login.png
dsq_thread_id:
  - 2433994764
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - Internet
  - Open Source
  - PHP
  - plugin
  - poll
  - theme
  - themes
  - WordPress
  - wordpress-plugin
  - wordpress-plugins
  - wordpress-theme
  - wordpress-themes

---
 

For some reason, WordPress will send a `200` [HTTP response status code][1], or `OK`, when a login attempt has failed. Why not send a `403` status code, which is designed specifically to say _you can&#8217;t be here_, or `forbidden`, actually. There&#8217;s even a better alternative to `403`, but stay with me.

I came about this bit of information while reading [this post by Konstantin Kovshenin][2]. And was able to confirm it myself by logging into this site incorrectly, as you can see in the featured image above. **wp-login.php** is returned as `200 OK` and is circled in red.

So, as [Konstantin][3] suggested, we can use this code to send a proper `403 Forbidden` status code on a failed login attempt:

<pre class="EnlighterJSRAW" data-enlighter-language="php" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">&lt;?php
function my_login_failed_403() {
    status_header( 403 );
}
add_action( 'wp_login_failed', 'my_login_failed_403' )
?></pre>

But why send a `403`, which is `Forbidden`? It&#8217;s not truly a forbidden page, as people have a legit reason to be there, even if they can&#8217;t remember their password.

So, sending `401 Unauthorized` as the HTTP response status code may be even better.

<pre class="EnlighterJSRAW" data-enlighter-language="php" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">&lt;?php
function my_login_failed_401() {
    status_header( 401 );
}
add_action( 'wp_login_failed', 'my_login_failed_401' );
?></pre>

So, you can use either of those, the **first chunk** to send a `403 Forbidden` response, and the **second** for sending a `401 Unauthorized` response code.

<div id="polls-21" class="wp-polls">
</div>

<div id="polls-21-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

Either could go in the **functions.php** file for your theme, or more likely, in [your WordPress functionality plugin][4].

You can find a good [list of HTTP response codes at the Mozilla Developer Network site][1].

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="6098"
					data-ulike-nonce="c9adb65b73"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_6098"></button><span class="count-box"></span>
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

 [1]: https://developer.mozilla.org/en-US/docs/HTTP/Response_codes
 [2]: http://kovshenin.com/2014/fail2ban-wordpress-nginx/
 [3]: http://kovshenin.com/
 [4]: http://longren.io/creating-a-wordpress-functionality-plugin/
 [5]: #