---
title: More WordPress and some FireFox
author: Tyler Longren
type: post
date: 2005-11-30T03:30:11+00:00
url: /more-wordpress-and-some-firefox/
views:
  - 2107
dsq_thread_id:
  - 1385916794
tags:
  - blog
  - blogs
  - firefox
  - firefox-1.5
  - mozilla
  - news
  - PHP
  - plugins
  - software
  - thunderbird
  - WordPress
  - wordpress-2
  - wordpress-2-0
  - wordpress-2.0

---
**UPDATE:** Get [SK2-WP2Compatibility][1], a plugin for Spam Karma 2. It fixes the comment count problem mentioned below when using Spam Karma 2 with WordPress 2.0. OK, just wanted to get that out in the open. Please continue.

Now that I&#8217;ve spent a little more time with WordPress 2.0 RC1, I&#8217;ve discovered a plugin compatibility problem that&#8217;s probably going to [destroy me][2]. [Spam Karma 2][3] causes some problems when updating the &#8220;comment\_count&#8221; value in the &#8220;wp\_posts&#8221; table. It doesn&#8217;t just cause problems displaying comment numbers, I had to manually updated that field for some posts. But, it&#8217;s not like this type of thing wasn&#8217;t expected. I&#8217;m not brave enough to run slackware-current on my main workstation anymore, this works for me though.  
<!--adsense-->

  
So, I can either use Spam Karma and not have any comment counts for new or updated posts, or I can just stop using Spam Karma. I really don&#8217;t want to let Spam Karma go. I&#8217;ve already seen about 200 trackback/comment spams since disabling Spam Karma earlier today. I really hope to see a new release of [Spam Karma][3] that works with WordPress 2.0. I guess this problem [was known about][4] a few weeks ago. I somehow didn&#8217;t notice it when I upgraded to 2.0 beta 1 and then to 2.0 beta 2.  
<!--adsense-->

  
Anybody know of a comment/trackback spam WordPress plugin that&#8217;s known to work with 2.0? There&#8217;s the list in the support forums, which also happens to discuss the Spam Karma problems. I may see if the latest [WordPress Hashcash][5] will work at all.

There is good news though, not really relating to WordPress though. [FireFox 1.5][6] stable is out! You can get FireFox 1.5 at the [new official home][7] of FireFox and Thunderbird, [Mozilla.com][7].

Also, my [favorite Mint Pepper][8] has been updated to work with [Mint 1.23][9]. I was thinking of downgrading to Mint 1.14 just so I could have the Outclicks Pepper. [Andrew Sutherland][8] couldn&#8217;t have picked a better time to release his updated pepper.

**CONTINUED UPDATE:** Too bad I didn&#8217;t [see this][10] about an hour ago. Looks like I&#8217;ll get to keep my Spam Karma thanks to [SK2-WP2Compatibility][1], a plugin for Spam Karma 2.

> SK2-WP2Compatibility is a plugin for Spam Karma 2. It has no effect without Spam Karma 2.0 or higher being already installed on your WordPress system.  
> This plugin has no spam fighting or spam killing abilities. Instead, it is intended to provide a way by which all users moving to WordPress 2.0 can enjoy the benefits of Spam Karma &#8211; without having to worry about WordPress 2.0 specific changes.

Might not need that SK2 plugin for too long, there&#8217;s word of a [Spam Karma 2.1][1] soon.  
<!--adsense#adsenseRefer-->

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2106"
					data-ulike-nonce="7c04b65797"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2106"></button><span class="count-box"></span>
  </div>
</div>

[][11]{.later-button-el}

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

 [1]: http://lair.fierydragon.org/2005/11/sk2-wp2compatibility/
 [2]: http://www.longren.org/archives/2033
 [3]: http://unknowngenius.com/blog/wordpress/spam-karma/
 [4]: http://wordpress.org/support/topic/49898#post-274619
 [5]: http://elliottback.com/wp/archives/2005/10/23/wordpress-hashcash-30-beta/
 [6]: http://www.blogsofwar.com/firefox_1_5_released
 [7]: http://www.mozilla.com/
 [8]: http://code.jalenack.com/archives/outclicks-pepper/
 [9]: http://www.haveamint.com/
 [10]: http://codex.wordpress.org/User:Matt/2.0_Plugin_Compatibility
 [11]: #