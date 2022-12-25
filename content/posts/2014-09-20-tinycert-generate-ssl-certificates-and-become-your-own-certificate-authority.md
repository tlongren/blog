---
title: 'TinyCert: Generate SSL Certificates And Become Your Own Certificate Authority'
author: Tyler Longren
type: post
date: 2014-09-20T12:39:59+00:00
url: /tinycert-generate-ssl-certificates-and-become-your-own-certificate-authority/
featured_image: /wp-content/uploads/2014/09/tinycert.png
dsq_thread_id:
  - 3034963529
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cloudflare
  - cool
  - digitalocean
  - Internet
  - Personal
  - Security
  - services
  - tools

---
A few days ago I moved longren.io to `https`. I didn&#8217;t pay for a certificate though like I would when setting up an e-commerce site or something else important.

I even get the little green lock symbol in the address bar, but I think this is mostly due to my use of [Cloudflare][1].

[TinyCert][2] is a service I discovered that lets you be your own [PKI][3]/[certificate authority][4]. It&#8217;s entirely free and provides you with a very nice interface for managing your certificates. The image below shows the interface for managing your certificates. The list on the right is a list of certificates, as you can see I&#8217;ve got one made up for longrendev.io, but haven&#8217;t put it in place quite yet.  
[<img loading="lazy" src="https://i1.wp.com/longren.io/wp-content/uploads/2014/09/tinycertinterface-1024x448.png?resize=700%2C306" alt="tinycertinterface" width="700" height="306" class="aligncenter size-large wp-image-7484" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/09/tinycertinterface.png?resize=1024%2C448&ssl=1 1024w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/09/tinycertinterface.png?resize=150%2C65&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/09/tinycertinterface.png?resize=300%2C131&ssl=1 300w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/09/tinycertinterface.png?resize=700%2C306&ssl=1 700w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/09/tinycertinterface.png?w=1175&ssl=1 1175w" sizes="(max-width: 700px) 100vw, 700px" data-recalc-dims="1" />][5]

The support from TinyCert is very good as well, I had a few questions regarding how their certificates would work with Cloudflare and they quickly cleared my questions up. SSL Labs from Qualys gives the [SSL certificate an &#8220;**A**&#8221; rating][6]. Should you use certificates from TinyCert in production? Probably not. I am, however, due to my use of Cloudflare.  
[<img loading="lazy" src="https://i1.wp.com/longren.io/wp-content/uploads/2014/09/ssl-300x223.png?resize=300%2C223" alt="ssl" width="300" height="223" class="aligncenter size-medium wp-image-7485" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/09/ssl.png?resize=300%2C223&ssl=1 300w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/09/ssl.png?resize=150%2C111&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/09/ssl.png?resize=700%2C521&ssl=1 700w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/09/ssl.png?w=936&ssl=1 936w" sizes="(max-width: 300px) 100vw, 300px" data-recalc-dims="1" />][7]

This post isn&#8217;t meant to show you how to install certificates or use TinyCert, it&#8217;s simply to make you aware of the tool and what can be done with it. TinyCert has a pretty [extensive FAQ][8], so should you have questions, which I&#8217;m sure you do, head on over and start reading. If you do need help installing the certificates from TinyCert, their [help center][9] does a nice job of providing instructions for Apache and Nginx based setups. 

Have fun with TinyCert, it&#8217;s a pretty awesome service that I&#8217;ll continue to use and will absolutely be donating to. **But please remember, TinyCert certificates should not be used for regular public websites and the service is not a substitute for a proper certification authority, but for self-signed certificates**. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7476"
					data-ulike-nonce="3092df049e"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7476"></button><span class="count-box"></span>
  </div>
</div>

[][10]{.later-button-el}

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

 [1]: http://cloudflare.com/
 [2]: https://www.tinycert.org/
 [3]: https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&cad=rja&uact=8&ved=0CDMQFjAA&url=http%3A%2F%2Fen.wikipedia.org%2Fwiki%2FPublic_key_infrastructure&ei=Db8cVJ3QNIinyATTn4KgDA&usg=AFQjCNHNBrqvvJMc9Pysi_eAtEEEqbVl-w&sig2=xmVHPkluQg0hUry6Cemppg&bvm=bv.75775273,d.aWw
 [4]: http://en.wikipedia.org/wiki/Certificate_authority
 [5]: https://i1.wp.com/longren.io/wp-content/uploads/2014/09/tinycertinterface.png?ssl=1
 [6]: https://www.ssllabs.com/ssltest/analyze.html?d=longren.io&s=162.159.240.220
 [7]: https://i0.wp.com/longren.io/wp-content/uploads/2014/09/ssl.png?ssl=1
 [8]: https://www.tinycert.org/faq
 [9]: https://www.tinycert.org/help
 [10]: #