---
title: Fix StanleyWP WordPress Theme Portfolio Grid
author: Tyler Longren
type: post
date: 2015-02-23T13:19:43+00:00
url: /fix-stanleywp-wordpress-theme-portfolio-grid/
featured_image: /wp-content/uploads/2015/02/wp-stanley.png
independent_publisher_primary_category:
  - WordPress
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
dsq_thread_id:
  - 3537468192
tags:
  - bootstrap
  - css
  - framework
  - Internet
  - JavaScript
  - Open Source
  - Personal
  - twitter bootstrap
  - WordPress
  - wordpress-theme
  - wordpress-themes

---
 

## Fix display of portfolio grid rows {.subtitle}

Back in September of 2014 I wrote about using the [StanleyWP WordPress theme][1] for a portfolio site. After I added some projects, I noticed the grid on the Portfolio page template wasn&#8217;t displaying rows correctly. I even noted it in my [original post][2], towards the end.

I&#8217;ve had a few people contact me about how to fix the StanleyWP portfolio grid issue, and earlier today [Arun left a comment][3] asking how to fix the grid issue.

You need to be using a child theme for this, it&#8217;s just good practice. If you don&#8217;t know how to create a child theme, [read my post on creating a child theme][4]. It&#8217;s really easy to do, but may require you to reset your menu or some widgets after changing to the child theme.

Anyway, [Arun confirmed][5] that [this gist][6] fixed the problem for him.  


Just save that code as `template-portfolio.php` and put it in your child theme directory. Your portfolio should now show three projects per row. No CSS or anything else needs to be modified, just that one page template.

Let me know if you have any issues or questions.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7902"
					data-ulike-nonce="c5dddebc78"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7902"></button><span class="count-box">2+</span>
  </div>
</div>

[][7]{.later-button-el}

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
    </p>
  </div>
  
  <div class='hire'>
    <h3>
      Leave some Feedback
    </h3>
    
    <p>
      Got a question or some updated information releavant to this post? Please, <a href='#respond' title='Leave a comment'>leave a comment</a>! The comments are a great way to get help, I read them all and reply to nearly every comment. Let's talk. 😀
    </p>
  </div>
  
  <div class='now-what-bottom-ad'>
    <h3>
      Longren.io is proudly hosted by <a href='https://www.digitalocean.com/?refcode=cbf49d0481c8'>DigitalOcean</a>
    </h3>
    
    <span class='do_link'><a href='https://www.digitalocean.com/?refcode=cbf49d0481c8' rel='nofollow' target='_blank'><img alt='DigitalOcean' border='0' src='https://i0.wp.com/longren.io/wp-content/uploads/2014/03/digitalocean.png?w=1100&#038;ssl=1' data-recalc-dims="1" /></a></span> <!--<h3>Need Cloud Monitoring? Try Mist.io!</h3><span class='do_link'><a href='http://mist.io/?ref=tyler' rel='nofollow' target='_blank'><img alt='Mist.io' border='0' src='https://i0.wp.com/longren.io/wp-content/uploads/2014/04/mistio.jpg?w=1100&#038;ssl=1' data-recalc-dims="1"></a></span>-->
  </div>
</div>

 [1]: http://gentsthemes.com/themes/stanleywp-twitter-bootstrap-wordpress-theme/
 [2]: https://longren.io/my-portfolio/
 [3]: https://longren.io/my-portfolio/#comment-1868808360
 [4]: https://longren.io/building-a-wordpress-child-theme/
 [5]: https://longren.io/my-portfolio/#comment-1868819255
 [6]: https://gist.github.com/tlongren/d90becc304cbb812e53e#file-template-portfolio-php
 [7]: #