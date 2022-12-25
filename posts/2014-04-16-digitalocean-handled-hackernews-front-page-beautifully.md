---
title: 'HackerNews Front Page: I Stayed Up'
author: Tyler Longren
type: post
date: 2014-04-16T14:02:05+00:00
url: /digitalocean-handled-hackernews-front-page-beautifully/
featured_image: /wp-content/uploads/2014/04/hn.png
full_width_featured_image:
  - 1
dsq_thread_id:
  - 2615577091
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - apache
  - apache2
  - cool
  - digital ocean
  - digitalocean
  - hosting
  - Internet
  - nginx
  - Personal

---
## Load (cpu and memory) was significantly lower than I expected {.subtitle}

Didn&#8217;t expect anything specific for load, but more load than what I did see, for sure.

A [post I made][1] hit the [front page of HackerNews][2] the other day. Here&#8217;s the [discussion at HackerNews][3]. Traffic was steady, For about five hours, there were between 50 and 250 users on the site at any given time.

I use two [DigitalOcean][4] droplets, one running Apache 2, the other for MySQL (mostly). The Apache 2 droplet is a 2GB droplet in the NYC2 datacenter and the MySQL droplet is a 1GB droplet in the same datacenter. They talk to each other over a private network.

I&#8217;ve really liked the setup so far, and without any tweaks to Apache or MySQL, both servers have performed quite well. I use a WordPress caching plugin and [CloudFlare][5], but that&#8217;s all there is for caching.

<figure id="attachment_6530" aria-describedby="caption-attachment-6530" style="width: 672px" class="wp-caption aligncenter">[<img loading="lazy" src="https://i1.wp.com/longren.io/wp-content/uploads/2014/04/cpu.png?resize=672%2C219" alt="CPU Usage" width="672" height="219" class="size-full wp-image-6530" srcset="https://i1.wp.com/www.longren.io/wp-content/uploads/2014/04/cpu.png?w=672&ssl=1 672w, https://i1.wp.com/www.longren.io/wp-content/uploads/2014/04/cpu.png?resize=150%2C48&ssl=1 150w, https://i1.wp.com/www.longren.io/wp-content/uploads/2014/04/cpu.png?resize=300%2C97&ssl=1 300w" sizes="(max-width: 672px) 100vw, 672px" data-recalc-dims="1" />][6]<figcaption id="caption-attachment-6530" class="wp-caption-text">CPU usage remained quite low, you can clearly see the HackerNews traffic.</figcaption></figure>

Eventually, one could expect thousands of users on a site at any given time. That greatly depends on the type of site, though.

At that point, you&#8217;d probably need [the power of Nginx, using it as a front-end (reverse) proxy to Apache][7].

I&#8217;m going to setup a [DigitalOcean droplet][4] to serve as a reverse proxy in the event I need to serve massive amounts of traffic. It&#8217;s sole job will be to run [Nginx][8].

I simply don&#8217;t need it right now, though. Unless this hits the front page of HackerNews and makes it further up the page. `;)`. Then I&#8217;ll be scrambling to get that Nginx box up. So, put me to work later.

<figure id="attachment_6538" aria-describedby="caption-attachment-6538" style="width: 639px" class="wp-caption aligncenter">[<img loading="lazy" src="https://i0.wp.com/longren.io/wp-content/uploads/2014/04/bandwidth.png?resize=639%2C216" alt="Bandwidth Usage" width="639" height="216" class="size-full wp-image-6538" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/bandwidth.png?w=639&ssl=1 639w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/bandwidth.png?resize=150%2C50&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/bandwidth.png?resize=300%2C101&ssl=1 300w" sizes="(max-width: 639px) 100vw, 639px" data-recalc-dims="1" />][9]<figcaption id="caption-attachment-6538" class="wp-caption-text">Highest bandwidth usage was 2.33Mbps. DigitalOcean can do a LOT more than that.</figcaption></figure>

I didn&#8217;t receive any alerts from [New Relic][10], [Mist.io][11], or [Uptime Robot][12], so all was good. I am, however, still going to prep some kind of solution with Nginx sitting in front of Apache, to at least serve static files.  


<div id="polls-27" class="wp-polls">
</div>

<div id="polls-27-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="6471"
					data-ulike-nonce="dd3b60809b"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_6471"></button><span class="count-box"></span>
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

 [1]: http://longren.io/poor-mans-vpn-with-a-cheap-vps/
 [2]: https://news.ycombinator.com/
 [3]: https://news.ycombinator.com/item?id=7586775
 [4]: https://www.digitalocean.com/?refcode=cbf49d0481c8
 [5]: http://cloudflare.com
 [6]: https://i1.wp.com/longren.io/wp-content/uploads/2014/04/cpu.png
 [7]: https://www.digitalocean.com/community/articles/how-to-configure-nginx-as-a-front-end-proxy-for-apache
 [8]: http://nginx.org/
 [9]: https://i0.wp.com/longren.io/wp-content/uploads/2014/04/bandwidth.png
 [10]: http://newrelic.com
 [11]: http://mist.io/
 [12]: http://uptimerobot.com/
 [13]: #