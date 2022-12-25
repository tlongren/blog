---
title: Dreamhost Has A Slow Network
author: Tyler Longren
type: post
date: 2006-09-08T23:10:15+00:00
url: /dreamhost-has-a-slow-network/
wjt_diPostTopic:
  - software
views:
  - 3420
ratings_users:
  - 2
ratings_score:
  - 10
ratings_average:
  - 5
dsq_thread_id:
  - 1553698737
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - blog
  - downtime
  - Dreamhost
  - dreamhost-down
  - dreamhost-outage
  - longren.org
  - network
  - outage
  - tech

---
The issues I spoke about in [_Poor Site Performance_][1] probably aren&#8217;t related to any content within this site, as I had previously thought. It&#8217;s more likely related to the shabby state of Dreamhosts network.

I am now blaming the Dreamhost network for the poor performance of this site for the following reasons.  
**  
1. Intermittence:** This one is simple. Sometimes single posts will load in a snap. Other times they take up to 30 seconds to display. Same with the index page, archives, about, and contact pages. The contact and about pages are relatively void of content. There&#8217;s really no reason for slowness or lag when loading those pages, there&#8217;s not much info to display there.

**2. Other Pages:** Other pages at the longren.org domain also load slow at times. Take [Mint][2] for example. The Mint dashboard fails to load or loads very slowly when this blog is also responding very slowly. It takes up to a minute to refresh some very basic peppers from within Mint.

**3. MySQL Is Usually OK:** If I&#8217;m not mistaken, Dreamhost has it&#8217;s MySQL databases on separate servers. In other words, a machine that serves http requests doesn&#8217;t server MySQL data at the same time, another entirely separate box would handle the MySQL responses. My thought here is that Dreamhost might have their MySQL serving machines on a different network entirely, one that might not be having issues the rest of their network is experiencing. I could be way off here though, entirely speculation.

[The Dreamhost Status site][3] has been unavailable for most of the day. There&#8217;s normally a blog hosted there. Currently, there&#8217;s simply a few paragraphs of text explaining the current situation:

> **Network downtime Monday Night (09/11)**  
> Monday night, we will upgrading our core networking equipment, which will result in some downtime of all services lasting approximately 30-45 minutes.  
> We&#8217;re expecting this to put an end to the network problems that were created by the power outages about a month ago..  
> &#8211; Sep. 8, 2006 3:30 p.m.
> 
> **Oops! Temporary Status Site**  
> We had a little goof and this will be our status site until the other machine can be resuscitated.  
> &#8211; Sep. 8, 2006 11:40 a.m.

So, as you can see, they&#8217;re relating this to [the downtime experienced a month or so back when a generator caught fire][4]. Hopefully the work they do on this coming Monday will fix the issues we&#8217;ve been having. It&#8217;s getting real old, real quick. Couldn&#8217;t happen at a worse time too, this site is starting to grow by great leaps and bounds. Hopefully growth won&#8217;t be affected by this poor performance.

**UPDATE:** This site was unreachable for about 12 hours lastnight/this morning. Here&#8217;s some new items that have been posted to dreamhoststatus.com:

> **Wilmington Failed Over**  
> Wilmingtons second network card, which carries internet traffic, decided to give up the ghost. The server is on shiny new hardware now and websites are already starting to serve again. Our apologies for the downtime.  
> &#8211; Sep. 9, 2006 1:24 p.m.
> 
> **Web Control Panel Issue Resolved**  
> The network issues causing slowness for the web control panel for the web control panel have now been resolved. The network overall is more responsive and we will continue to make minor changes to keep everything working as well as possible. The major maintenance on Monday night will be essentially a complete replacement and upgrade of one of our core routers. In the meantime, we have been re-routing as much of our network traffic as possible through our other core router to improve overall performance.  
> &#8211; Sep. 9, 2006 2:48 a.m.
> 
> **Web Control Panel Slowness**  
> The network issues are also causing problems with the Web Control Panel for several users. We are looking into this and hope to have everything restored shortly.  
> &#8211; Sep. 8, 2006 8:56 p.m.
> 
> **Network Problems Today**  
> We have been experiencing Network Problems today. These problems are the same problems that have actually been happening since we first reported problems with our network. Unfortunately these problems have gotten worse today and are causing a majority of the downtime and slowness issues you are reporting today. These problems, and our attempts at fixing them, have been an ongoing effort. The maintenance Monday Night will be a big step towards resolving these problems completely. We are currently working on the network and all servers having problems and hope to improve the situation soon. Sorry about the downtime, we hope to have this all resolved soon.  
> &#8211; Sep. 8, 2006 5:45 p.m.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2238"
					data-ulike-nonce="76e37fb4a9"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2238"></button><span class="count-box"></span>
  </div>
</div>

[][5]{.later-button-el}

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

 [1]: http://www.longren.org/2006/09/06/poor-site-performance/
 [2]: http://www.haveamint.com/
 [3]: http://dreamhoststatus.com/
 [4]: http://www.longren.org/2006/07/28/dreamhost-generators-caught-fire/
 [5]: #