---
title: HTML5Press Lightbox Effect
author: Tyler Longren
type: post
date: 2011-08-24T15:07:25+00:00
url: /html5press-lightbox-effect/
featured_image: /wp-content/uploads/2011/08/html5press_slimbox-e1314197553750-604x270.png
views:
  - 58
dsq_thread_id:
  - 1385932259
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - html5press
  - Internet
  - Open Source
  - Personal
  - poll
  - WordPress

---
The most recent poll I posted here indicates that most HTML5Press users would like to see a lightbox-type effect built into HTML5Press.  


<div id="polls-4" class="wp-polls">
  <p style="text-align: center;">
    <strong>Would you like a lightbox-type effect built into HTML5Press?</strong>
  </p>
  
  <div id="polls-4-ans" class="wp-polls-ans">
    <ul class="wp-polls-ul">
      <li>
        Yes <small>(91%, 32 Votes)</small><div class="pollbar" style="width: 91%;" title="Yes (91% | 32 Votes)">
        </div>
      </li>
      
      <li>
        No <small>(9%, 3 Votes)</small><div class="pollbar" style="width: 9%;" title="No (9% | 3 Votes)">
        </div>
      </li>
    </ul>
    
    <p style="text-align: center;">
      Total Voters: <strong>35</strong>
    </p>
  </div>
  
  <input type="hidden" id="poll_4_nonce" name="wp-polls-nonce" value="a279b34ab0" />
</div>

<div id="polls-4-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

  
I thought about adding a lightbox-type feature to HTML5Press with CSS3 but ended up settling on [Slimbox2 instead][1]. Slimbox2 is a very small clone of the popular [Lightbox][2] image overlay effect.

I have implemented slimbox2 for featured images mostly. So, if you click on a featured image when viewing a single post, the large image will show in the slimbox.

It will also work with images embedded directly in your posts. You won&#8217;t have to worry about adding rel=&#8221;lightbox&#8221; to your image links either, as I&#8217;ve [added some code to take care of that][3] automatically.

I haven&#8217;t officially released a new version of HTML5Press that includes this new feature, but if you&#8217;re interested you can [grab a development version of HTML5Press from Github][4].

You&#8217;ll need to enable the lightbox effect via the HTML5Press Options page in your WordPress Dashboard. The effect is turned off by default.

**This post is sponsored by:**  
Comindware &#8211; is an innovative company that produces unique business software and [online collaboration tools][5] for any industry. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2975"
					data-ulike-nonce="b05bfb784e"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2975"></button><span class="count-box"></span>
  </div>
</div>

[][6]{.later-button-el}

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

 [1]: http://www.digitalia.be/software/slimbox2
 [2]: http://www.lokeshdhakar.com/projects/lightbox2/
 [3]: https://github.com/tlongren/html5press/commit/f0710936d447a00b5d9c9ad159e34fb555374bbe
 [4]: https://github.com/tlongren/html5press
 [5]: http://www.comindware.com/
 [6]: #