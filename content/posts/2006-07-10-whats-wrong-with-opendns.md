---
title: What’s Wrong With OpenDNS?
author: Tyler Longren
type: post
date: 2006-07-10T23:10:14+00:00
url: /whats-wrong-with-opendns/
ratings_users:
  - 2
ratings_score:
  - 8
ratings_average:
  - 4
views:
  - 4141
dsq_thread_id:
  - 1385905868
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - apache
  - blog
  - blogs
  - dns
  - everydns
  - httpd
  - network
  - network-security
  - OpenDNS
  - Security
  - tech
  - technology
  - www

---
[OpenDNS][1] is surely going to prove to be a useful tool for those not intimately familiar with the internet. OpenDNS, provides some unique functionality compared with other DNS servers in that it detects typos and prevents phishing. For example, say you type http://www.longren.og into your browser. That URL obviously doesn&#8217;t exist, notice the .og at the end? OpenDNS will recognize the typo and will redirect the user to http://www.longren.org.

Smart huh? Yes, but it could [have it&#8217;s drawbacks][2]. [This post][2] highlights what could be a potential security risk in OpenDNS. It has to deal with intrusion detection systems (IDS) not realizing which URL is actually being requested. That post uses the [mod_speling apache httpd module][3] as an example.

> If I send a request for indexh.tml, mod_speling detects the mistake and will serve back index.html. The problem is any security products like an IDS/IPS won&#8217;t have this intelligence to try and &#8220;fix&#8221; the request before they analyze it. The IDS/IPS simply sees and logs a request for indexh.tml Modspelling, like this feature in OpenDNS, allows an attacker to side step the attack signatures on a IDS/IPS to exploit a site because the web server will &#8220;fix&#8221; the attack once it reaches its target.

<!--adsense-->

  
I disagree with the logic behind the authors claims. Why? Simply because I have a feeling OpenDNS was built with that taken into consideration. I&#8217;m betting there&#8217;s some sort of database internally that lets every piece of the network know exactly what is being served when a typo is detected. Everything from the IDS boxes to the DNS servers themselves. Maybe I totally missed the point of what that post was trying to get across.

Another thing OpenDNS should work on ASAP is transparency. I&#8217;d really like to know the false positive rate on phishing sites. How many legitimate sites get flagged as a phishing site? A publicly available reporting system would also be nice. Something to show DNS changes in particular would be nice for helping to maintain the integrity of the database.

But, I&#8217;m sure these questions will be answered in the near future, after all, today is the company&#8217;s first day with exposure to the &#8220;public&#8221;. There&#8217;s already mention of a [new feature on the most recent post][4] at the OpenDNS blog.

> One important feature which is not yet available, but will be soon, is self-service control over the DNS settings. Ryan’s article, understandably, doesn’t mention this capability, since it’s not yet live.
> 
> The point? We’re going to put more control in your hands, so if you want to turn off features like typo correction or phishing prevention, you’ll be able to. Account management is the top priority now, to help demonstrate the power of control over your DNS. We think transparency and control will show you (not just tell) that we’re making the right choices. 

Ryan&#8217;s article is of course [the article that was in Wired this morning][5]. See, they&#8217;re already taking steps to provide more transparency, hopefully it will continue.

[Harper Reed][6] is also a bit skiddish with OpenDNS still, like me. I think OpenDNS has great intentions though, so I&#8217;m not too worried. Founder of OpenDNS, David Ulevitch, already has a pretty outstanding reputation in the internet community, probably due mostly to the success of EveryDNS. OpenDNS is out to do good on the internet, just like EveryDNS. That doesn&#8217;t mean they can&#8217;t do harm, as we saw with [Blue Security][7].

I&#8217;m pretty sold on OpenDNS overall. I put their DNS servers in my DHCP server config tonight after I got home from work. And the Nevada office as well as a couple servers in Ankeny are using OpenDNS now too. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2164"
					data-ulike-nonce="8a33af918a"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2164"></button><span class="count-box"></span>
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

 [1]: http://www.opendns.com/
 [2]: http://www.memestreams.net/users/acidus/blogid9121142/
 [3]: http://httpd.apache.org/docs/1.3/mod/mod_speling.html
 [4]: http://blog.opendns.com/2006/07/10/first-article-about-opendns-appears-in-wired-news/
 [5]: http://www.wired.com/news/technology/0,71345-0.html?tw=wn_index_1
 [6]: http://www.nata2.org/2006/07/10/opendns/
 [7]: http://en.wikipedia.org/wiki/Blue_Security#Spammers.27_backlash
 [8]: #