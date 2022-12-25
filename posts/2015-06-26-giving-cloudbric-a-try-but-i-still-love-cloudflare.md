---
title: Giving Cloudbric A Try, But I Still Love Cloudflare
author: Tyler Longren
type: post
date: 2015-06-26T07:39:13+00:00
url: /giving-cloudbric-a-try-but-i-still-love-cloudflare/
featured_image: /wp-content/uploads/2015/06/cloudbric.png
independent_publisher_primary_category:
  - Maintenance
dsq_thread_id:
  - 3880820245
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cloudflare
  - cool
  - digitalocean
  - hosting
  - Internet
  - maintenance
  - Noteworthy
  - Personal
  - Security
  - services
  - tools
  - waf
  - web application firewall

---
## Going to try Cloudbric here for a while to see how exactly it compares to Cloudflare

Longren.io will be unavailable for possibly up to 48 hours. As soon as I&#8217;ve published this post, I&#8217;ll be updating my nameservers to point to Cloudbric, almost feels like cheating on Cloudflare, they&#8217;ve been very good to me.

I&#8217;ve been using [Cloudflare][1] for quite a while, nearly since it became available to the public. I love them and all the services they provide, especially with a Pro (or Enterprise) account. Cloudflare costs money though (if you want certain added protections), and many smaller websites don&#8217;t use a lot of bandwidth and aren&#8217;t provided the protections they should receive with Cloudflare.

Cloudbric aims to solve that by providing all the features Cloudflare provides (from what I&#8217;ve been told at least) for free as long as your site doesn&#8217;t use more than 4GB of bandwidth per month. I only have a few Pro sites with Cloudflare (longren.io being one of them), but am trying to cut back on the number of online services I pay for monthly, so this makes sense on a financial level if nothing else.

I&#8217;d never heard of [Cloudbric][2] until they got in touch with me via direct message on [Twitter][3] and introduced me to their services. They appear to provide everything that Cloudflare&#8217;s Enterprise service provides, glad they saw one of my tweets praising Cloudflare and decided to get in touch.

Cloudbric has been around for a while (15 years or so I believe) and I talked to one of their reps quite a bit about how what they provide is better than Cloudflare (other than the usage based cost, of course).

Here&#8217;s what he said:

<blockquote class="wp-block-quote">
  <p>
    1. Unlike other website protection services including Cloudflare, Cloudbric provides full-coverage website protection. Even though Web Application Firewall (WAF) and DDoS Protection features are crucial for website protection, these options cost at least $200/month from Cloudflare. Cloudflare&#8217;s free plan does not protect web application layer 3, 4, and 7, which makes it pointless.
  </p>
  
  <p>
    2. Our usage-based plan, rather than options plan, allows even free users to enjoy the most comprehensive security service. There are no charges for extra add-ons or features for more security. Users can enjoy all the features for FREE up to 4GB of traffic monthly.
  </p>
</blockquote>

Here&#8217;s a handy table from the Cloudbric website showing a feature comparison with similar providers like [Cloudflare][1], [Sitelock][4], and [Incapsula][5].  


<table class="wp-block-table">
  <tr>
    <th>
      FEATURES
    </th>
    
    <th>
      Cloudbric
    </th>
    
    <th>
      Incapsula
    </th>
    
    <th>
      SiteLock
    </th>
    
    <th>
      Cloudflare
    </th>
  </tr>
  
  <tr>
    <td>
      Advanced DDoS Protection(Layer 3, 4, 7)
    </td>
    
    <td>
      <strong>FREE</strong>
    </td>
    
    <td>
      $299 /mo
    </td>
    
    <td>
      Enterprise
    </td>
    
    <td>
      $200 /mo
    </td>
  </tr>
  
  <tr>
    <td>
      PCI-Certified Web Application Firewall(WAF)
    </td>
    
    <td>
      <strong>FREE</strong>
    </td>
    
    <td>
      $59 /mo
    </td>
    
    <td>
      $299 /mo
    </td>
    
    <td>
      $20 /mo
    </td>
  </tr>
  
  <tr>
    <td>
      Global Content Delivery Network
    </td>
    
    <td>
      <strong>FREE</strong>
    </td>
    
    <td>
      $19 /mo
    </td>
    
    <td>
      $99 /mo
    </td>
    
    <td>
      $20 /mo
    </td>
  </tr>
  
  <tr>
    <td>
      Web Opimization
    </td>
    
    <td>
      <strong>FREE</strong>
    </td>
    
    <td>
      $19 /mo
    </td>
    
    <td>
      $99 /mo
    </td>
    
    <td>
      $200 /mo
    </td>
  </tr>
  
  <tr>
    <td>
      OWASP Core Rule Set
    </td>
    
    <td>
      <strong>FREE</strong>
    </td>
    
    <td>
      $59 /mo
    </td>
    
    <td>
      $99 /mo
    </td>
    
    <td>
      $20 /mo
    </td>
  </tr>
  
  <tr>
    <td>
      Reputation-based Threat Protection
    </td>
    
    <td>
      <strong>FREE</strong>
    </td>
    
    <td>
      $59 /mo
    </td>
    
    <td>
      $299 /mo
    </td>
    
    <td>
      FREE
    </td>
  </tr>
  
  <tr>
    <td>
      Board Spam Protection
    </td>
    
    <td>
      <strong>FREE</strong>
    </td>
    
    <td>
      $59 /mo
    </td>
    
    <td>
      X
    </td>
    
    <td>
      X
    </td>
  </tr>
  
  <tr>
    <td>
      Block Visitors by IP or country
    </td>
    
    <td>
      <strong>FREE</strong>
    </td>
    
    <td>
      $59 /mo
    </td>
    
    <td>
      X
    </td>
    
    <td>
      FREE
    </td>
  </tr>
  
  <tr>
    <td>
      Login Protection
    </td>
    
    <td>
      <strong>FREE</strong>
    </td>
    
    <td>
      $59 /mo
    </td>
    
    <td>
      X
    </td>
    
    <td>
      X
    </td>
  </tr>
  
  <tr>
    <td>
      SSL Support
    </td>
    
    <td>
      <strong>FREE</strong>
    </td>
    
    <td>
      $19 /mo
    </td>
    
    <td>
      FREE
    </td>
    
    <td>
      FREE
    </td>
  </tr>
</table>

Figured I&#8217;d try it out on this site as it gets the most traffic out of my personal sites, and if everything&#8217;s cool, I&#8217;ll eventually be moving all clients over to Cloudbric. Just wish they had a way to import existing DNS records, some of my domain names have at least 50 sub-domains.

Longren.io subscribers will get this post via email, but longren.io could be down for up to 48 hours while stuff updates. I&#8217;ll update this post or maybe write a new one after I&#8217;ve used Cloudbric for a few days. You should at least [check them out][2], especially if you&#8217;re using Cloudflare for a site that doesn&#8217;t get enough traffic to make it worth paying for.

I really don&#8217;t want to leave Cloudflare, but if Cloudbric stacks up, I&#8217;m afraid I&#8217;ll have to.

**Update:** After updating nameservers for longren.io to Cloudbric, an SSL issue was found. I went back to Cloudflare immediately, and within about an hour Cloudbric&#8217;s engineering team had a solution worked out. It sounds like they&#8217;ll be rolling the fix out on Monday June 29. So until then, longren.io will be on Cloudflare. I&#8217;ll post info about the issue in detail after Cloudbric has officially announced it or made the fix active.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="8079"
					data-ulike-nonce="89e736fd7c"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_8079"></button><span class="count-box">7+</span>
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

 [1]: https://cloudflare.com/
 [2]: https://www.cloudbric.com
 [3]: https://twitter.com/tlongren/
 [4]: https://www.sitelock.com/
 [5]: https://www.incapsula.com/
 [6]: #