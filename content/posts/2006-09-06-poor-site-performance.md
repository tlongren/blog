---
title: Poor Site Performance
author: Tyler Longren
type: post
date: 2006-09-06T14:02:57+00:00
url: /poor-site-performance/
ratings_users:
  - 1
ratings_score:
  - 5
ratings_average:
  - 5
views:
  - 3211
dsq_thread_id:
  - 2396658902
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - Internet
  - longren.org
  - monitoring
  - performance
  - site24x7
  - software
  - www

---
[<img alt="Poor Response Time" title="Poor Response Time" style="float: left;" align="left" src="https://i2.wp.com/www.longren.org/wp-content/uploads/2006/09/poorsiteperformancegraph.jpg?w=1100" data-recalc-dims="1" />][1]Take a look at the photo shown there. I don&#8217;t like it, at all. I&#8217;ve been using [Site24x7][2] for the last few days to monitor various websites I run. It&#8217;s really handy and has brought to my attention a few things I wasn&#8217;t expecting. Namely, this site performs very poorly, which I&#8217;ve noticed more and more in the last few weeks.

OK, this site, longren.org, is hosted at Dreamhost. The Slackware Blog is of course, hosted at wordpress.com. And the other site in the image, is one for work. The site for work has better &#8220;response&#8221; times than both longren.org and the Slackware Blog. This took me by surprise because the work site is hosted on a Qwest DSL 1Mbit line.

[<img alt="Poor Response Time Comparison" title="Comparison" style="float: left;" align="left" src="https://i2.wp.com/www.longren.org/wp-content/uploads/2006/09/poorsiteperformancecomparison.jpg?w=1100" data-recalc-dims="1" />][3]I have a feeling the poor response time is mostly due to grabbing data from external sources, such as Google and Blogrolling. However, I don&#8217;t really include much content from external sources. Perhaps the small number of images causes this site to have much slower response times. The Slackware Blog and the work site are very light on images compared to this site. I never post images in posts at the Slackware Blog.

Anyway, I guess a 4500 millisecond response time isn&#8217;t too terrible, it&#8217;s about 4.5 seconds. Over the last couple days, the response time has gone down to around 2500 milliseconds, or 2.5 seconds. This site does have a larger amount of data to pull for every page, so I guess increased response times here are to be expected. Maybe I&#8217;m just worrying about nothing. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2231"
					data-ulike-nonce="41322b34db"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2231"></button><span class="count-box"></span>
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

 [1]: http://www.flickr.com/photos/tlongren/231218299/
 [2]: http://site24x7.com "Site24x7"
 [3]: http://www.flickr.com/photos/tlongren/233041608/
 [4]: #