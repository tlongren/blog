---
title: Digg Integrator Plugin Fix
author: Tyler Longren
type: post
date: 2006-09-23T17:10:04+00:00
url: /digg-integrator-plugin-fix/
ratings_score:
  - 11
ratings_average:
  - 3.67
views:
  - 7450
ratings_users:
  - 3
DiggURL:
  - http://www.digg.com/software/Digg_Integrator_Plugin_Fix
wjt_diPostTopic:
  - software
dsq_thread_id:
  - 1385918617
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - blog
  - blogging
  - code
  - coding
  - digg
  - PHP
  - plugin
  - programming
  - scripting
  - WordPress
  - wordpress-plugins

---
[The Digg Integrator plugin v1.1 for WordPress][1] hasn&#8217;t been working correctly. The author, WildBil, has been working on a fix for the last week or so. I got tired of waiting for a fix lastnight and took it upon myself to create one.

In addition to the referring Digg URL not being detected, I think there&#8217;s also a problem when submitting a site to Digg that has a &#8220;Preferred Digg Topic&#8221; set. The preferred topic is never sent along to Digg because the variable containing the preferred topic isn&#8217;t being called correctly in diggIntegrator.php.

All of the fixes I mention here are to be made within the wjt_diggThisPost function inside diggIntegrator.php. That function starts on line 225.

Now, moving on. The problem with the referring digg URL not being captured is extremely simple, I think. The function that captures the referring digg URL is simply not being called correctly. Basically, it&#8217;s not being run when it needs to. Look at line 278 in diggIntegrator.php:  
<!--more-->

<pre>wjt_diDetect; // looks for incoming links from digg and helps this function continue appropriately</pre>

See, it&#8217;s calling the wjt_diDetect function, partially. I modified that line to look like this:

<pre>wjt_diDetect(); // looks for incoming links from digg and helps this function continue appropriately</pre>

Notice the added parentheses at the end of the wjt_diDetect function? Simply adding those parentheses will cause the referring Digg URL to be detected and inserted as meta data for the given post. Just as should happen.

Now for the preferred topic not being sent to Digg. This is a very simple fix as well. Take a look at line 298 in diggIntegrator.php:

<pre>'&topic='.diggTopic. //collect the topic (doesn't need encoding)</pre>

See the .diggTopic. part? Well, &#8220;diggTopic&#8221; isn&#8217;t a variable in diggIntegrator.php, obviously. However &#8220;$diggTopic&#8221; is. To get the plugin to send the preferred topic to Digg when digging a new URL, change line 298 to look like this:

<pre>'&topic='.$diggTopic. //collect the topic (doesn't need encoding)</pre>

Notice all that&#8217;s added is the dollar sign ($) to the front of &#8220;diggTopic&#8221;. Pretty simple.

If you&#8217;d like to download a fixed copy of diggIntegrator.php, you can [get it from right here][2]. I have only made the changes listed above to that script. I&#8217;m sure [WildBil will release a more all-inclusive fix][3] as there may be a few things I missed here. All I know is once I made the changes above, the incoming Digg URL was successfully detected and inserted. I tested on multiple URL&#8217;s of mine.

Let me know if this works for you guys or not.

**UPDATE:** WildBil [posted version 1.2 of the Digg Integrator plugin][4]. Instead of downloading that fixed diggIntegrator.php above, just head over to his site to get the newest version. Version 1.2 includes the fixes I mentioned here and a new feature that includes a sample of the button generated by wjt_diggThisPost. [Go get it][4]. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2246"
					data-ulike-nonce="8d2d356886"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2246"></button><span class="count-box"></span>
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

 [1]: http://bill2me.com/digg-integrator/digg-integrator-v1_1/
 [2]: http://www.longren.org/diggIntegrator.phps
 [3]: http://bill2me.com/2006/08/06/digg-integrator-v11c/
 [4]: http://bill2me.com/2006/09/23/digg-integrator-v12/
 [5]: #