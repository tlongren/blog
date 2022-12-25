---
title: 'Belt: A Handful Of Tools For PHP Developers'
author: Tyler Longren
type: post
date: 2014-04-19T10:35:01+00:00
url: /belt-a-handful-of-tools-for-php-developers/
featured_image: /wp-content/uploads/2014/04/php-belt.png
dsq_thread_id:
  - 2623145330
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cool
  - git
  - GitHub
  - Internet
  - Open Source
  - opensource
  - Personal
  - PHP
  - tools

---
## Clean and well-documented source {.subtitle}

[Belt][1] is a really handy, and relatively new tool set for PHP developers. It&#8217;s [initial commit was only 9 days before][2] the date this post was published.

However, it still looks very usable and rather mature. Code has been added at a pretty quick pace, there&#8217;s been 102 commits since Belt&#8217;s release on GitHub, a little over a week ago.

It&#8217;s release under the [MIT license][3], so it&#8217;s compatible with the GPL and can safely used in [WordPress][4] themes and functions, if you want them included in the official repositories. 

Basically, you just include `belt` and use it&#8217;s built in methods/functions to do certain things that would take a bit more work using straight PHP. For example, to get the maximun of an array of numbers, do this:

<pre class="lang:php decode:true " ><?php Belt::max([1, 2, 3]) ?></pre>

A value of `3` will be returned, because it&#8217;s the max value there.

And from the readme, a [list of what Belt offers][5].

  * 60+ useful functions
  * ability to use the facade Belt or a dedicated component (e.g. BeltUtilities)
  * fully tested
  * source code is clean and documented

Seems like it offers some pretty useful functions, and it looks really easy to use. I&#8217;ve been looking for a solid PHP base to use and this may just be it. Anyone got any other suggestions? I&#8217;ve heard a lot about Skeleton for PHP. 

Searching for &#8220;skeleton&#8221; on GitHub, then filtering for PHP, gives [a LOT of result][6]s, over 1,000 results to be more precise. So, maybe I&#8217;ll browse there for a while before making a decision.

Any suggestions can be [left in the comments][7]. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="6576"
					data-ulike-nonce="ba9998ab41"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_6576"></button><span class="count-box"></span>
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

 [1]: https://github.com/ilya-dev/belt/tree/master
 [2]: https://github.com/ilya-dev/belt/commit/dd37e4662279ed1906fec82937b4969276e1026a
 [3]: https://github.com/ilya-dev/belt/blob/master/LICENSE
 [4]: http://wordpress.org/
 [5]: https://github.com/ilya-dev/belt/blob/master/README.md
 [6]: https://github.com/search?l=php&q=skeleton&ref=reposearch
 [7]: #response
 [8]: #