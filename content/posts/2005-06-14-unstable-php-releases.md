---
title: Unstable PHP Releases
author: Tyler Longren
type: post
date: 2005-06-14T15:39:55+00:00
url: /unstable-php-releases/
views:
  - 984
dsq_thread_id:
  - 2026592803

---
[PHP][1] released PHP 5.1.0 Beta 1 a few days ago. Today they [released PHP 4.4.0 RC1][2]. Below is what the PHP website had to say about the release candiadte for 4.4.0.

> This is a bug-fix only release, the increased middle digit is needed because this release changes PHP&#8217;s Internal API that causes existing third-party binary extensions to be incompatible with the new version.
> 
> This release address a major problem within PHP concerning references. If references where used in a wrong way, PHP would often create memory corruptions which would not always surface and be visible. In other cases it can cause variables and objects to change type or class. If you encountered strange behavior like this, this release might fix it.
> 
> Besides addressing this reference related bug, 46 other bugs are fixed. Please test this release and report any bugs or problems in our bugsystem (after searching first). You can find 4.4.0 RC1 at <http://qa.php.net/~derick/>

I&#8217;ve been debating on wether or not to upgrade to either of these. I probably won&#8217;t as there&#8217;s no [hardened-php][3] patch for these releases yet. If anything I&#8217;d upgrade to the latest 5.1.0 beta as I&#8217;m already running 5.0.4. I don&#8217;t see any reason to go back to the 4.x branch.

Anyway, [Arthur Wiebe][4] [provides a list of changes][5] in PHP 5.1.0 Beta 1. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="1919"
					data-ulike-nonce="003b2454e7"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_1919"></button><span class="count-box"></span>
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

 [1]: http://www.php.net/
 [2]: http://qa.php.net/~derick/
 [3]: http://www.hardened-php.net/
 [4]: http://artooro.blogspot.com/
 [5]: http://artooro.blogspot.com/2005/06/php-510-beta-1-coming.html
 [6]: #