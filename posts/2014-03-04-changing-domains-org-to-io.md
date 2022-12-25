---
title: Changing Domains, .org to .io
author: Tyler Longren
type: post
date: 2014-03-04T08:17:32+00:00
url: /changing-domains-org-to-io/
featured_image: /wp-content/uploads/2014/03/google.png
dsq_thread_id:
  - 2356326144
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - digitalocean
  - hosting
  - Internet
  - Personal
  - WordPress

---
## Maybe Google won&#8217;t hate me anymore {.subtitle}

A bunch of scummy sites are using some of my old WordPress themes. The themes have links to longren.org in the footer, I think Google hates me for it, I dunno though. It started about 3 years ago. When all was good, organic search referrals from [Google][1] were around 15,000 unique visitors per month.

Now, however, the story is much different. In all, Google is throwing me about 800 unique visitors a month from organic search. I believe it has something to do with all of the incoming links to longren.org from low quality websites. I really have no idea though and am not about to hire some SEO company to fix it up or take the time to [disavow][2] hundreds of thousands of links.

I&#8217;ve got longren.org forwarding to longren.io now, but will eventually turn that off and just start from scratch, I guess. Unless Google can help, but that&#8217;s not probably likely.

<blockquote class="twitter-tweet" data-width="550" data-dnt="true">
  <p lang="en" dir="ltr">
    <a href="https://twitter.com/mattcutts?ref_src=twsrc%5Etfw">@mattcutts</a> Possible that you could see if <a href="http://t.co/8Yhe0mdXV6">http://t.co/8Yhe0mdXV6</a> got a search penalty a few years ago? Curious more than anything. Thanks!
  </p>
  
  <p>
    &mdash; Tyler Longren (@tlongren) <a href="https://twitter.com/tlongren/status/440607608320167936?ref_src=twsrc%5Etfw">March 3, 2014</a>
  </p>
</blockquote>



Oh well. Only change will be the new .io TLD. It&#8217;ll be nice having a new domain, even though I&#8217;ll keep the old one around forever most likely.

Doing the forwarding so <longren.org/work-with-me/> will end up at <longren.io/work-with-me/> with 301 redirects all around. This is all that was needed in the `.htaccess` file.

<pre class="lang:default decode:true " >Redirect 301 / http://longren.io/</pre>

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5771"
					data-ulike-nonce="ea7b89a9e9"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5771"></button><span class="count-box"></span>
  </div>
</div>

[][3]{.later-button-el}

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

 [1]: http://google.com
 [2]: https://www.google.com/webmasters/tools/disavow-links-main
 [3]: #