---
title: Passwds.io Source Available on GitHub
author: Tyler Longren
type: post
date: 2014-12-03T15:58:55+00:00
url: /passwds-io-source-available-on-github/
featured_image: /wp-content/uploads/2014/12/passwds-github.png
independent_publisher_primary_category:
  - Services
dsq_thread_id:
  - 3286908861
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cool
  - css
  - digitalocean
  - freelance
  - git
  - GitHub
  - hosting
  - Internet
  - JavaScript
  - Open Source
  - passwds.io
  - Personal
  - PHP
  - Security
  - services
  - tools

---
## Now on GitHub {.subtitle}

Took a bit longer than I wanted, but the source for [passwds.io][1] is up [on GitHub now][2].

It&#8217;s extremely simple, using [Twitter Bootstrap][3], straight [PHP][4], [jQuery][5], and the [jQuery prettySocial plugin][6] for the social buttons at the bottom of the site.

Passwords are generated using [pwgen-php from Superwayne][7]. pwgen-php was [forked a couple years ago][8] by [Roderik van der Veer][9], which I was unaware of.

I&#8217;ll be updating to the somewhat newer [pwgen-php library from Roderik][8] at some point.

Basically, an [AJAX request is sent][10] to a [PHP file][11], grabbing the requested passwords, and then the results are displayed.

Pretty simple. Let me know if you have suggestions or questions. Please be kind, I threw this together in [about an hour one evening][12]. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7783"
					data-ulike-nonce="f0091a3cd8"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7783"></button><span class="count-box"></span>
  </div>
</div>

[][13]{.later-button-el}

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

 [1]: https://passwds.io/
 [2]: https://github.com/tlongren/passwds.io
 [3]: http://getbootstrap.com/
 [4]: http://php.net
 [5]: http://jquery.com
 [6]: https://github.com/sonnyt/prettySocial
 [7]: https://code.google.com/p/pwgen-php/
 [8]: https://github.com/roderik/pwgen-php
 [9]: https://github.com/roderik
 [10]: https://github.com/tlongren/passwds.io/blob/master/js/process.js
 [11]: https://github.com/tlongren/passwds.io/blob/master/process.php
 [12]: https://longren.io/introducing-passwds-io/
 [13]: #