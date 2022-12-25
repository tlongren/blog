---
title: Add Post Thumbnails To wp-svbtle
author: Tyler Longren
type: post
date: 2013-12-10T19:13:41+00:00
url: /add-post-thumbnails-to-wp-svbtle/
featured_image: /wp-content/uploads/2013/12/Svbtle-e1386702161847.png
dsq_thread_id:
  - 2041849682
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - GitHub
  - Internet
  - Open Source
  - Personal
  - WordPress

---
I&#8217;ve always enjoyed the [svbtle][1] design. Shortly after it became a _thing_, the [wp-svbtle theme was made][2]. It does a really nice job of replicating the look and feel of the svbtle.com site. In the [wp-svbtle readme][3], it even states that it&#8217;s an extremely unoriginal idea, but that&#8217;s kinda the point.

As you can tell, I&#8217;m using wp-svbtle here on longren.org now. I made a small change to the theme to allow featured images (post thumbnails) on posts. Pretty much all my posts from the last year+ have a featured image set, and I still wanted those to display, even while using wp-svbtle. You can see the featured image for this post in the top left, it&#8217;s a circle and clicking on it will take you to the post permalink.

After I made the modifications to allow featured images, I [sent a pull request][4] to the official wp-svbtle repo on GitHub. Could be a while before it&#8217;s merged (if it&#8217;s even merged at all), the wp-svbtle repo hasn&#8217;t been updated in over 4 months. So, we&#8217;ll see.

If development on it has truly stalled for good, I&#8217;ll probably update my master branch to include the featured images support. Right now, you can find it in the [&#8220;post-thumbnails&#8221; branch][5] at my [GitHub fork][6].

Also, if you&#8217;re interested in WordPress in general, why not check out my book, [_WordPress Multisite Administration_][7]? 🙂 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="4850"
					data-ulike-nonce="e854cc8fbe"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_4850"></button><span class="count-box"></span>
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

 [1]: http://svbtle.com
 [2]: https://github.com/themeskult/wp-svbtle
 [3]: https://github.com/themeskult/wp-svbtle/blob/master/README.md
 [4]: https://github.com/themeskult/wp-svbtle/pull/167
 [5]: https://github.com/tlongren/wp-svbtle/tree/post-thumbnails
 [6]: https://github.com/tlongren/wp-svbtle/
 [7]: http://www.packtpub.com/wordpress-multisite-administration/book
 [8]: #