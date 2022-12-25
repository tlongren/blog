---
title: Horrible Repsonse Time
author: Tyler Longren
type: post
date: 2006-12-05T03:14:20+00:00
url: /horrible-repsonse-time/
views:
  - 2410
dsq_thread_id:
  - 1690797935
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - Dreamhost
  - Internet
  - longren.org
  - monitoring
  - performance
  - Personal
  - site24x7
  - software
  - www

---
<a href="https://i0.wp.com/farm1.static.flickr.com/119/314434179_a2422dc5c2_o.png" title="Site24x7 Showing A Slow longren.org" rel="thumbnail"><img loading="lazy" src="https://i1.wp.com/static.flickr.com/119/314434179_a2422dc5c2_m.jpg?resize=240%2C172" width="240" height="172" alt="longrenOrgEvenSlower" align="left" data-recalc-dims="1" /></a>Longren.org has been really, really slow the last week or so. This site has never been this slow to load, even when I was hosting it out of my house on my cable connection. Granted, I didn&#8217;t get the traffic back then that I do now, it still shouldn&#8217;t be this slow.

[Last time longren.org was being slow as shit][1], I posted an image of a graph from Site24x7, like I&#8217;ve done in this post. The response time in the earlier image is horrible, 4510 ms, but that&#8217;s a lot lower than I&#8217;m seeing now. As you can see from the image above in this post, the current average response time over the last 7 days is 6614 ms.

This has to be a result of something going on at Dreamhost. I say that because sometimes pages on longren.org will load up in a snap. Most of the time though they take between 15 and 30 seconds to load. Even sending queries to the database is slower than normal. Database queries are usually done being executed within 1 or 2 seconds. Lately, it&#8217;s been taking 5 to 9 seconds. Something is definitely up. Perhaps I will submit a support ticket to Dreamhost tomorrow. Yay. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2282"
					data-ulike-nonce="b3eb3248e6"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2282"></button><span class="count-box"></span>
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

 [1]: http://www.longren.org/2006/09/06/poor-site-performance/
 [2]: #