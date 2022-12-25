---
title: The Impending Storm
author: Tyler Longren
type: post
date: 2005-07-05T16:37:07+00:00
url: /the-impending-storm/
views:
  - 1003
dsq_thread_id:
  - 1940320491

---
The Internet Storm Center is warning that the internet environment is ripe for a major security event. The [ISC diary warns][1] of the impending storm. If said storm does come to pass, many sites will be vulnerable, but not this one. The problems arises in PHP&#8217;s xml-rpc functions. WordPress makes heavy use of these functions for ping/trackbacks and updating RSS feeds.

Netcraft has a [pretty detailed account][2] of the flaw. I first saw this yesterday on [Slashdot][3]. 

Here&#8217;s a little quote from Netcraft.

> Many popular PHP-based blogging, wiki and content management programs can be exploited through a security hole in the way PHP programs handle XML commands. The flaw allows an attacker to compromise a web server, and is found in programs including [PostNuke][4], [WordPress][5], [Drupal][6], [Serendipity][7], [phpAdsNew][8], [phpWiki][9] and [phpMyFAQ][10], among others.
> 
> The flaw affects the XML-RPC function, which has many uses in web applications, including &#8220;ping&#8221; update notifications for RSS feeds. PHP libraries that allow applications to exchange XML data using remote procedure calls(RPC) fail to fully check incoming data for malicious commands. The affected libraries, including PHPXMLRPC and Pear XML-RPC, are included in many interactive applications written in PHP.

I took the steps necessary to upgrade my xml-rpc version. Did so by running this command on my web server: &#8220;pear upgrade XML_RPC&#8221;. I also upgraded [hardened-php][11]. The new version of Hardened-PHP fixes this xml-rpc problem. The new version of hardened-php is 0.3.0. Last version was 0.2.7. The [hardened-php site][11] also got a make-over. I think it looks very nice. It&#8217;s much easier to find the issues that are addressed in each hardened-php patch. As long as hardened-php is around, I&#8217;m going to use it. I&#8217;m glad they&#8217;re watching out for me. It&#8217;s great to see they&#8217;ve included a patch for this xml-rpc flaw already.

**UPDATE:** Although the report on Netcraft and the others say WordPress is affected, it isn&#8217;t if you&#8217;re running 1.5.1.3. [Matt][12], a WordPress developer, says they use &#8220;different, more secure libraries for XML-RPC&#8221;. He just [made a post][13] clearing up the confusion that WordPress is affected. [Steve Mallett][14] is on top of things too. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="1935"
					data-ulike-nonce="862daf41fc"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_1935"></button><span class="count-box"></span>
  </div>
</div>

[][15]{.later-button-el}

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

 [1]: http://isc.sans.org/diary.php?date=2005-07-03
 [2]: http://news.netcraft.com/archives/2005/07/04/php_blogging_apps_vulnerable_to_xmlrpc_exploits.html
 [3]: http://it.slashdot.org/article.pl?sid=05/07/04/2153224&tid=95&tid=172&tid=169
 [4]: http://news.postnuke.com/Article2699.html
 [5]: http://wordpress.org/development/2005/06/wordpress-1513/
 [6]: http://drupal.org/
 [7]: http://blog.s9y.org/archives/36-CRITICAL-BUGFIX-RELEASE-Serendipity-0.8.2.html
 [8]: http://phpadsnew.com/two/nucleus/index.php?itemid=45
 [9]: http://sourceforge.net/forum/forum.php?forum_id=478443
 [10]: http://www.phpmyfaq.de/advisory_2005-06-29.php
 [11]: http://www.hardened-php.net/
 [12]: http://photomatt.net
 [13]: http://photomatt.net/2005/07/05/xml-rpc-vulnerability/
 [14]: http://dev.fooworks.com/2005/07/05/update-your-php-apps-now/
 [15]: #