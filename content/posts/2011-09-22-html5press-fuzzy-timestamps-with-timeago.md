---
title: 'HTML5Press: Fuzzy Timestamps with Timeago'
author: Tyler Longren
type: post
date: 2011-09-22T21:58:17+00:00
url: /html5press-fuzzy-timestamps-with-timeago/
featured_image: /wp-content/uploads/2011/09/timeago.png
views:
  - 54
dsq_thread_id:
  - 1542154889
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - html5press
  - Internet
  - poll
  - WordPress

---
I&#8217;ve [added][1] [an][2] [option][3] to HTML5Press to enable fuzzy timestamps for posts and pages. Fuzzy timestamps display how long ago an item was published, instead of showing the date and time it was published.

For example, [this post][4] about [Minus][5] was published on 9/19/2011. Fuzzy timestamps would cause that to be displayed as &#8220;3 days ago&#8221; instead of showing the actual date. Come tomorrow, that post will show that it was published &#8220;4 days ago&#8221;.

You can still see the actual date by mousing over the fuzzy timestamp.

<div id="polls-8" class="wp-polls">
</div>

<div id="polls-8-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

I implemented this with the [timeago jQuery plugin][6]. This feature will be available once HTML5Press 2.1 is released, which will probably be sometime before October. If you&#8217;d like to take it for a test drive now, you can [download HTML5Press 2.1-rc1 from Github][7]. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="3050"
					data-ulike-nonce="abebb44289"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_3050"></button><span class="count-box"></span>
  </div>
</div>

[][8]{.later-button-el}

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

 [1]: https://github.com/tlongren/html5press/commit/086b0e3787a5a2b8a272eefe5f58ea046eb3d4c7
 [2]: https://github.com/tlongren/html5press/commit/86975e24e5e9142832944d0e19a7c2a44bd3dc5d
 [3]: https://github.com/tlongren/html5press/commit/79e52c6bb3ab64c5aef4caa00045f3d6bbbe3c0c
 [4]: http://www.longren.org/minus-an-alternative-to-dropbox/
 [5]: http://min.us/rh2pAm3
 [6]: http://timeago.yarp.com/
 [7]: https://github.com/tlongren/html5press/archives/master
 [8]: #