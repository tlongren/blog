---
title: OpenDNS Speed
author: Tyler Longren
type: post
date: 2006-07-14T14:38:11+00:00
url: /opendns-speed/
views:
  - 1830
dsq_thread_id:
  - 1385931832
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - adware
  - blog
  - blogs
  - dns
  - illegal
  - news
  - OpenDNS
  - Security
  - software
  - spyware
  - virus
  - weather
  - www

---
[Wikipedia defines Adware][1] as &#8220;Adware or advertising-supported software is any software package which automatically plays, displays, or downloads advertising material to a computer after the software is installed on it or while the application is being used.&#8221;

[This guy makes some good points][2], the OpenDNS as Adware idea not being one of them though. He&#8217;s had some issues with the typo fix feature of OpenDNS and the OpenDNS search page coming up when it shouldn&#8217;t.

> So what happens when it doesn’t know the IP address you ask? Well sometimes it returns no answers
> 
> javila@BeanMac ~ $ dig verizonn.com @208.67.222.222
> 
> ;; flags: qr rd ra; QUERY: 1, ANSWER: 0, AUTHORITY: 0, ADDITIONAL: 0
> 
> And sometimes it gives you back their server. (asdverizon.com. 1 IN A 208.67.219.40) any request to 208.67.219.40 results in a search the attempted url being ran through their systems. If im not misunderstood, they make their money off of adds displayed at this time… therefore, the more they don’t catch, the more money they make on advertising? Ok so I guess for their software it “Pays to be stupid”

Simply because an application doesn&#8217;t provided the expected results doesn&#8217;t mean it&#8217;s adware. OpenDNS seems like the kind of company who is out to stop adware and other sorts of internet baddies. That post is worth a read, it does a nice job of bringing to light some problems in OpenDNS. And, I don&#8217;t think the guy was actively trying to take the &#8220;OpenDNS is Adware&#8221; stand, he did file that post under &#8220;[Talking Shit][3]&#8221; after all. heh.

Another interesting [OpenDNS related post comes from Thomas Ptacek][4]. Thomas has noticed OpenDNS actually takes longer to resolve some domains than, say, your ISP&#8217;s DNS servers.

> 74ms longer via OpenDNS. How much of that is network latency? You could turn off recursion, but OpenDNS doesn’t support it, so instead query for OpenDNS’s own names:
> 
> nsping -z opendns.com 208.67.222.222  
> + [ 22 ] 55 bytes from 208.67.222.222: 261.771 ms [ 192.468 san-avg ]
> 
> 41ms. Weak evidence that it takes OpenDNS 33ms longer to look up random names at Google on my DSL connection? Note also that all the OpenDNS queries “succeed”, because OpenDNS sends you to a landing page for typos.

Some pretty interesting comments going on at that post too. David Ulevitch and Thomas might end up getting together to do some testing on DNS caches and overall performance. [David made a comment][5] in my [previous post on OpenDNS][6] in which he explains some of the new features they&#8217;re working on:

> I agree 100% about us needing to be more transparent. The three biggest things we are working on right now are:  
> 1) Getting account preferences up and running so people can just enable and disable the various features they are working on.  
> 2) Providing a much clearer understanding of where our phishing data comes from and what happens if we make a mistake  
> 3) Bringing up our London datacenter and adding in a bunch of peering and other network connectivity to our existing sites.

I&#8217;ve really only witnessed one problem with OpenDNS. This is a prime example, try navigating to <http://www.tehserver.us/>. It takes you to the OpenDNS search page, right? Well, the first link displayed on the search page is really where I want to go. So, I click the first link and I&#8217;m taken right back to the OpenDNS search page I was just on. So, there&#8217;s apparently no way for me to get to www.tehserver.us using OpenDNS. Granted, tehserver.us isn&#8217;t totally legitimate, it&#8217;s definitely not breaking any sort of laws. Perhaps the spellcheck is getting confused. The domain is tehserver.us, not theserver.us.

I&#8217;ve been using OpenDNS for about 5 days now. I am going to do some testing tonight at home to see if OpenDNS actually serves up info quicker than my ISP&#8217;s DNS servers. I will post the results and how I went about testing. That is, provided I have power at home, there&#8217;s been some awesome storms rolling through the last couple days. A welcome event for the farmers around here though.  
**  
UPDATE:** I can get to tehserver.us with no problem now, I never even see the OpenDNS search page. [David mentioned][7] he&#8217;s opened a bug in bugzilla for the developers to check out. He also mentioned [this post on OpenDNS by Greg Keene][8]. Greg takes a look at OpenDNS and fears even one security breach could make OpenDNS disappear:

> My concerns? The obvious, security and security. Will temptation to generate advertising overcome their &#8216;do good&#8217; nature? We&#8217;ll have to see. A huge, obvious hole is their own security. If they get hacked, then their users are effectively exposed &#8212; don&#8217;t underestimate this. I&#8217;d like to get more people using them so we can really find how good they are. My thought is that one security breach could kill these guys, even an exposed exploit would be a very bad thing.
> 
> Give it a try and let me know what you think.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2168"
					data-ulike-nonce="c4127b4f98"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2168"></button><span class="count-box"></span>
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

 [1]: http://en.wikipedia.org/wiki/Adware
 [2]: http://www.beanfuzz.com/wordpress/?p=56
 [3]: http://www.beanfuzz.com/wordpress/?cat=9
 [4]: http://www.matasano.com/log/363/third-party-dns-caches-considered-a-blog-post/
 [5]: http://www.longren.org/archives/2164#comment-26811
 [6]: http://www.longren.org/archives/2164
 [7]: http://www.longren.org/archives/2168#comment-27018
 [8]: http://blog.gregkeene.com/keene/2006/07/opendns_a_conve.html
 [9]: #