---
title: Measure Page Scrolling in Google Analytics
author: Tyler Longren
type: post
date: 2014-03-26T13:40:31+00:00
url: /measure-page-scrolling-in-google-analytics/
featured_image: /wp-content/uploads/2014/03/scroll-depth.png
dsq_thread_id:
  - 2511555319
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cool
  - GitHub
  - google
  - google-analytics
  - Internet
  - JavaScript
  - jquery
  - Personal

---
## A Google Analytics plugin for measuring page scrolling {.subtitle}

Earlier today I came across a [Google Analytics plugin called Scroll Depth][1], developed by [Rob Flaherty][2]. Here&#8217;s how he describes Scroll Depth:

> Scroll Depth is a small Google Analytics plugin that allows you to measure how far down the page your users are scrolling. It monitors the 25%, 50%, 75%, and 100% scroll points, sending a Google Analytics Event at each one.
> 
> You can also track when specific elements on the page are scrolled into view. On a blog, for example, you could send a Scroll Depth event whenever the user reaches the end of a post.
> 
> The plugin supports Universal Analytics, Classic Google Analytics, and Google Tag Manager.

Scroll Depth is available [on GitHub][3] and on [it&#8217;s project page][1]. Getting it setup is easy, the only two requirements are Google Analytics and jQuery.

Below is a basic setup.

<pre class="lang:xhtml decode:true " >&lt;script src="jquery.scrolldepth.min.js"&gt;&lt;/script&gt;
&lt;script&gt;
$(function() {
  $.scrollDepth();
});
&lt;/script&gt;</pre>

Just be sure to include `jquery.scrolldepth.min.js` and the call to `.scrollDepth()` is made after Google Analytics has been loaded up.

There&#8217;s a number of options you can pass, too:. I especially like the `elements` option. It allows you to define a unique element to record scroll events for. So, if you want to track when users scroll to the footer of a post in WordPress, you could easily set that up!

<pre class="lang:js decode:true " >$.scrollDepth({
  minHeight: 2000,
  elements: ['#comments', 'footer'],
  percentage: false,
  userTiming: false,
  pixelDepth: false
});</pre>

As stated, the only requirements are Google Analytics and jQuery. If it doesn&#8217;t seem to be working for you, ensure that Scroll Depth isn&#8217;t being loaded before your Google Analytics tracking code. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="6228"
					data-ulike-nonce="1334c15cab"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_6228"></button><span class="count-box"></span>
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

 [1]: http://scrolldepth.parsnip.io/
 [2]: http://parsnip.io/
 [3]: https://github.com/robflaherty/jquery-scrolldepth
 [4]: #