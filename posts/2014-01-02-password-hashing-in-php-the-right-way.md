---
title: Password Hashing in PHP, The Right Way™
author: Tyler Longren
type: post
date: 2014-01-03T02:02:18+00:00
url: /password-hashing-in-php-the-right-way/
featured_image: /wp-content/uploads/2014/01/php.png
dsq_thread_id:
  - 2088499879
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - GitHub
  - Internet
  - Open Source
  - Personal
  - PHP
  - Security

---
I took time recently to read up on best methods for generating and storing user password hashes. The &#8216;base&#8217; I often use for websites, in PHP, hasn&#8217;t been updated in a while and needed some updating on the login side of things. [This article at crackstation.net][1] was pretty much everything I used while updating how my base hashes user passwords and generates and stores the salts.

Previously, I was using the same, static salt for everyone, but found that to be a less than optimal practice, from a security standpoint. Everything I did was pretty heavily based on [the PHP source provided][2] in the crackstation.net piece.

Using a random salt means that you need to keep track of it somehow, and that&#8217;s usually done by saving the salt in the database, along with the password hash and other user info. But, if your database is compromised, the salt used in creating the password hash is readily available for the attacker. And that&#8217;s not a good thing.

So, in addition to the stuff described in the Crackstation.net article, I also use a static, but still random string that gets appended to each random salt. Now, if my database is compromised, but my filesystem is still secured, attackers won&#8217;t have the entire salt. The static string that we add to the random salt should only be accessible from our PHP source, which is on the still secure filesystem.

If you can, use a third-party library for password hashing, like [phpass][3], which is used in projects like [WordPress][4] and [Vanilla][5]. It&#8217;s very popular, and for good reason.

Another good library for passwords in PHP would probably be [PHP Password Library][6]. I&#8217;ve never used it myself, but it looks like it&#8217;d be really easy to integrate into existing code, and can be installed via [Composer][7].

Also, if you&#8217;re able to run PHP 5.5.x, you can make use of the [new password hashing functions][8], [password_hash()][9] and [password_verify()][10]. [This article at Sitepoint][11] gives a good overview of the new functions.

If you&#8217;re on an older version of PHP (anything below PHP 5.5.0) and would like to use the new [password hashing functions][8], you should look at [ircmaxwell/password_comapt on github][12]. It provides forward-compatibility with the [password_* functions][8] found in PHP 5.5.

So, there&#8217;s no shortage of good options for helping out with password hashing. And if you do need to roll your own, you can use a function like [openssl\_random\_pseudo_bytes()][13] or [mcrypt\_create\_iv][14] to generate the salt.

I&#8217;m generating random salts using openssl\_random\_pseudo_bytes() and using [MySQL&#8217;s sha2 function][15] for password hashing. sha2() was added in MySQL 5.5.5, so it probably won&#8217;t be available to you if you&#8217;re using an earlier version. Although I believe many linux distributions have a patched version. 

Did I mess something up? Please let me know if I&#8217;ve missed something or if I&#8217;m just totally off base somewhere. Comments are open.

Edit: As [Matt noted in the comments][16], sha2 isn&#8217;t a very good choice, so I&#8217;m <del datetime="2014-01-03T03:40:10+00:00">going to use</del> now using the [password_comapt library][12], [hello bcrypt][17]. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5034"
					data-ulike-nonce="ad6a6f0db4"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5034"></button><span class="count-box"></span>
  </div>
</div>

[][18]{.later-button-el}

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

 [1]: https://crackstation.net/hashing-security.htm
 [2]: https://crackstation.net/hashing-security.htm#phpsourcecode
 [3]: http://www.openwall.com/phpass/
 [4]: http://ryan.boren.me/2007/12/17/secure-cookies-and-passwords/
 [5]: https://github.com/vanillaforums/Garden/tree/master/library/vendors/phpass/
 [6]: http://rchouinard.github.io/phpass/
 [7]: http://getcomposer.org/
 [8]: http://php.net/password
 [9]: http://www.php.net/manual/en/function.password-hash.php
 [10]: http://www.php.net/manual/en/function.password-verify.php
 [11]: http://www.sitepoint.com/hashing-passwords-php-5-5-password-hashing-api/
 [12]: https://github.com/ircmaxell/password_compat
 [13]: http://us3.php.net/openssl_random_pseudo_bytes
 [14]: http://php.net/manual/en/function.mcrypt-create-iv.php
 [15]: http://dev.mysql.com/doc/refman/5.5/en/encryption-functions.html#function_sha2
 [16]: http://www.longren.org/password-hashing-in-php-the-right-way/#comment-1184994403
 [17]: http://codahale.com/how-to-safely-store-a-password/
 [18]: #