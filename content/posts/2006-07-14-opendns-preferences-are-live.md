---
title: OpenDNS Preferences Are Live
author: Tyler Longren
type: post
date: 2006-07-14T17:48:28+00:00
url: /opendns-preferences-are-live/
views:
  - 2
dsq_thread_id:
  - 1385933227
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - blog
  - blogs
  - dns
  - Internet
  - news
  - OpenDNS
  - preferences
  - software
  - tech
  - technology

---
I just noticed [the OpenDNS preferences page][1] is up and running. It&#8217;s pretty basic, but now you can enable or disable typo correction and phishing protection. The configuration is done based on IP address, so if you don&#8217;t have a static or persistent IP address, you might be out of luck. I don&#8217;t have a static IP at home, but I&#8217;ve managed to keep the same one for a little over a year now.

Here&#8217;s a screenshot of the preferences page:  
[<img loading="lazy" src="https://i2.wp.com/static.flickr.com/56/189524049_f9b378f7af_o.png?resize=455%2C293" width="455" height="293" alt="OpenDNSPrefsSmall" data-recalc-dims="1" />][2]

Obviously, there&#8217;s not much there at this time. But look at the little information box in the top right. It mentions they&#8217;ll be adding more preferences there over time. It looks like they plan to have user accounts soon too, so you can manage preferences not based solely on your IP. Fun fun!

**UPDATE:** In my last [post on OpenDNS][3], I mentioned I was having trouble getting to http://www.tehserver.us/. The problem seemed to resolve itself, when I was suddenly able to hit tehserver.us with no problem. However, come Monday morning, I&#8217;m unable to load tehserver.us again. Even when I type http://www.tehserver.us/Home, the direct link to the homepage, I get the OpenDNS search page. OpenDNS search successfully finds the site, but when I click on the search result, I&#8217;m taken back to the OpenDNS search page instead of being taken to tehserver.us. The really odd thing is that I can reach tehserver.us with no problem from home. Not so from work though. I&#8217;d think a traceroute to tehserver.us would be nearly identical from my house and from the office, since the two are about 3 city blocks away from each other. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2169"
					data-ulike-nonce="cdf57f80b0"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2169"></button><span class="count-box"></span>
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

 [1]: http://www.opendns.com/prefs/
 [2]: http://www.flickr.com/photos/tlongren/189524049/ "Photo Sharing"
 [3]: http://www.longren.org/archives/2168
 [4]: #