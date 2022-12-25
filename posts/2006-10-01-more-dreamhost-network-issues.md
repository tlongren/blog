---
title: More Dreamhost Network Issues
author: Tyler Longren
type: post
date: 2006-10-01T21:40:57+00:00
url: /more-dreamhost-network-issues/
views:
  - 1
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
dsq_thread_id:
  - 4695303973
tags:
  - Dreamhost
  - dreamhost-outage
  - hosting
  - Internet
  - longren.org
  - Personal
  - WordPress
  - www

---
[Dreamhost is recovering][1] from yet another network outage. Apparently a switch had issues and they had to take a few servers off that switch. Supposedly the servers were moved over to another temporary switch so they&#8217;d have network access, but I haven&#8217;t had access to longren.org for at least 2 hours now.

> We have moved the servers in the affected rack to knew switches in other racks temporarily while we get a new switch in place. We are working on recovery efforts now on servers which may be down. The list of affected servers is:
> 
> Arrow, mel, caesar, herod, alondra, overland, rossmore, oxnards, cerritos, selma, nala, demeter, jarvis. This is a mix of 3 MySQL servers and the rest webservers.

Longren.org is hosted on oxnard unfortunately, that box seems to have a lot of issues, even when the Dreamhost network is functioning properly. They&#8217;ve now managed to replace the problematic switch and are working on bringing servers back online.

> Sorry about no timestamp before, it’s 12:36 Pacific time (-0800? I never could keep track of daylight savings time.)
> 
> We have completely replaced the switch and are working on getting the servers back online. All networking cables are back in their regularly scheduled switch ports. 

<!--adsense-->

  
I always get a kick out of the angry comments that show up on the Dreamhost Status blog whenever a fairly widespread problem occurs. Of course, Dreamhost [hasn&#8217;t had great reliability][2] in [the last few months][3]. I feel bad for those trying to run a business with Dreamhost.

One quick note, [WordPress][4] 2.0.5 [should be here soon][5].

**UPDATE:** Apparently there&#8217;s still trouble. Now Dreamhost is saying the servers affected are still behaving abnormally. This box, oxnard, doesn&#8217;t appear to be affected though, for once! They&#8217;re still [updating that same post][1] at the Dreamhost Status blog:

> Wierdness is afoot. The servers are still exhibiting the same problems, we have even moved two of them into our new datacenter and it’s the same deal. It’s only specific servers in half of one of our racks.

**UPDATE 2 @ 8:52 PM CST:** Dreamhost now says all their problems are over. Which they do appear to be. I believe the [K2 site is hosted][6] at Dreamhost, I noticed it was down for a while but has since been revived. Here&#8217;s the update from the [Dreamhost Status blog][1]:

> As of 1700 Pacific time (GMT-0800 or so, 5PM), we think the issues with this rack are behind us. We moved some machines to new hardware and this seems to have fixed the problems. We will be looking in to this more on monday, and doing some extensive testing on that hardware to make sure it was the root cause of the problem.

<!--adsense-->

  
Hopefully this was just a minor fluke and we don&#8217;t see any more problems. Like I said before, Dreamhost has been less than stable these last couple months. Honestly though, I have noticed this site loads much quicker since [Dreamhost fought with their network last time][2]. Still, there&#8217;s [a lot of recent posts categorized][7] as &#8220;system outages&#8221; at the Dreamhost Status blog. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2252"
					data-ulike-nonce="bb71822b98"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2252"></button><span class="count-box"></span>
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

 [1]: http://www.dreamhoststatus.com/2006/10/01/problems-with-networking/
 [2]: http://www.longren.org/2006/09/08/dreamhost-has-a-slow-network/
 [3]: http://www.longren.org/2006/07/28/dreamhost-generators-caught-fire/
 [4]: http://www.wordpress.org/
 [5]: http://wp-community.org/2006/10/01/episode-7-diggcom-wpcom-vip-hosting-what-plug-ins-do-you-use/
 [6]: http://www.getk2.com/
 [7]: http://www.dreamhoststatus.com/category/system-outages/
 [8]: #