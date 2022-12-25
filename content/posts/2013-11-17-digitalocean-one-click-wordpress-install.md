---
title: DigitalOcean One-Click WordPress Install
author: Tyler Longren
type: post
date: 2013-11-18T00:12:38+00:00
url: /digitalocean-one-click-wordpress-install/
featured_image: /wp-content/uploads/2013/11/DigitalOcean-Control-Panel.png
dsq_thread_id:
  - 1974986342
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - digital ocean
  - Internet
  - Linux
  - Personal
  - WordPress

---
I&#8217;ve been using [DigitalOcean][1] a LOT lately. Disclaimer: That first link will give me referral credit if you do end up using DigitalOcean. I&#8217;ve used a small droplet from them for a while now to host a [non-exit Tor relay][2], it runs $5 a month. They frequently [give out][3] [promo codes][4] on [Twitter][5], too, sometimes [worth a couple months of free hosting][6].

I recently moved this site to a new 1GB DigitalOcean droplet, and [used their one-click WordPress install][7] to do it. Some things had changed when deploying new droplets since I had created my first droplet a few months ago. The most noticeable change was the addition of pre-built images of various types, including one for a WordPress installation, as you can see in the images associated with this post.

They&#8217;ve got one-click installs for WordPress, various environments including LAMP and Ruby on Rails, both available on various Linux distributions. They&#8217;ve even got one for [Ghost][8], the new blog system built with Node.js. I really like how they&#8217;ve implemented the whole thing, deploying a new droplet for a WordPress install seriously takes a few minutes, and that&#8217;s including SSHing into the new droplet and finishing up with WordPress install.

I&#8217;ve been really happy with DigitalOcean so far. Don&#8217;t think I&#8217;ve experienced any downtime, at least none that me or various monitoring services have noticed, lol. Since you can get promo codes, and a short bit of free hosting, it can&#8217;t hurt to [try them out][1]. Their servers start at $5/month with 512MB RAM and 20GB SSD Disk, with 1TB of data transfer. Even without the promo codes, their prices are really attractive, at all levels.  


<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="4786"
					data-ulike-nonce="0a5aafcaf7"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_4786"></button><span class="count-box"></span>
  </div>
</div>

[][9]{.later-button-el}

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

 [1]: https://www.digitalocean.com/?refcode=cbf49d0481c8
 [2]: http://www.longren.org/tor-is-important-for-privacy-and-the-internet/
 [3]: https://twitter.com/digitalocean/status/390197040896290817
 [4]: https://twitter.com/digitalocean/status/368079162378293248
 [5]: https://twitter.com/digitalocean
 [6]: http://blog.vpsstat.us/posts/digitalocean-support-first
 [7]: https://www.digitalocean.com/community/articles/one-click-install-wordpress-on-ubuntu-12-10-with-digitalocean
 [8]: https://github.com/tryghost/Ghost
 [9]: #