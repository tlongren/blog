---
title: Version 0.0.3 of jQuery Sticky Alerts Plugin Now Available
author: Tyler Longren
type: post
date: 2014-04-24T13:00:10+00:00
url: /version-0-0-3-of-jquery-sticky-alerts-plugin-now-available/
featured_image: /wp-content/uploads/2014/04/newversion.png
dsq_thread_id:
  - 2631966405
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - GitHub
  - Internet
  - JavaScript
  - jquery
  - jquery plugin
  - Open Source
  - opensource
  - Personal
  - plugin

---
I&#8217;ve released version 0.0.3 of my [Sticky Alerts jQuery plugin][1]. It&#8217;s [available on GitHub][2] and is [now indexed at plugins.jquery.com][3].

I&#8217;ve added a feature to remember if the bar has been closed or not. This is done via cookies, and there&#8217;s an option to set. The option, `cookieRememberDays`, default to `2`. If you want to disable it (ie: bar will appear every time the page is loaded no matter what), you need to set `cookieRememberDays` to a value of ``.

To keep the **bar closed for 7 days**, do something like this:

<pre class="lang:js decode:true " >$('#alert-container').stickyalert({
  barFontColor:'#eee',
  barColor:'#222',
  barFontSize: '1.1rem',
  barText:'Hey, need some web work done? Give me a shout!',
  barTextLink:'http://longren.io/work-with-me/',
  cookieRememberDays: '7'
});</pre>

To **keep it as-is, and make the bar open on every page load**, do this:

<pre class="lang:js decode:true " >$('#alert-container').stickyalert({
  barFontColor:'#eee',
  barColor:'#222',
  barFontSize: '1.1rem',
  barText:'Hey, need some web work done? Give me a shout!',
  barTextLink:'http://longren.io/work-with-me/',
  cookieRememberDays: '0'
});</pre>

Head on [over to GitHub][4] for a download link, [or click here to download version 0.0.3 directly from the GitHub tag][2]. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="6643"
					data-ulike-nonce="89e1259ae9"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_6643"></button><span class="count-box"></span>
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

 [1]: http://longren.io/sticky-alerts-a-new-tiny-jquery-plugin/
 [2]: https://github.com/tlongren/jquery-sticky-alert/archive/0.0.3.zip
 [3]: http://plugins.jquery.com/sticky-alert/
 [4]: https://github.com/tlongren/jquery-sticky-alert/
 [5]: #