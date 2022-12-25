---
title: 'Heroku: Depriving Your Free Dyno of Sleep'
author: Tyler Longren
type: post
date: 2013-07-24T19:34:37+00:00
url: /heroku-depriving-your-free-dyno-of-sleep/
featured_image: /wp-content/uploads/2013/07/Heroku-Apps.png
dsq_thread_id:
  - 1536949019
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - heroku
  - howto
  - Internet
  - Open Source
  - paas
  - PHP
  - php-code

---
 

I&#8217;ve been using [Heroku][1] more and more, but not for anything really valuable to me. I mostly use it for hosting one-off projects that are low traffic. A lot of times, it&#8217;ll take 30 seconds or so for the site hosted on Heroku to respond, while the [Heroku dyno][2] is woken up. If your site goes without any traffic for a certain period of time, it will [go to sleep][3].

Heroku does this to save server resources, which is a logical thing for them to do. Sometimes though, I don&#8217;t want to wait to see my site, even if I only have a free account.

I&#8217;ve seen a lot of tutorials on how to do this with Ruby, but no language-agnostic way of doing it. I also haven&#8217;t seen any way of doing this with PHP. There&#8217;s 2 methods you can use to keep your site from going to sleep.

### 1. UptimeRobot

This is the easiest and quickest way to keep your app awake, and is language-agnostic. [UptimeRobot][4] is a free service that monitors your sites. When you&#8217;re adding a new site to monitor in UptimeRobot, make sure to set the monitor type to &#8220;HTTP(s)&#8221;. UptimeRobot will check to make sure your site is up every 5 minutes, which will prevent your site from sleeping.

### 2. Heroku Scheduler

This method is a little more involved, but is probably the Heroku-preferred method.

This topic has been [covered][5] [many][6] [times][7], but always seems to focus on Ruby apps. So here&#8217;s something that will work for everyone.

While you&#8217;re viewing your app resources on the Heroku dashboard, click the &#8220;Get Add-ons&#8221; link. Add the **Heroku Scheduler** add-on to your app, it&#8217;s free.

Go back to managing your app&#8217;s resources on the Heroku dashboard, then click &#8220;Heroku Scheduler Standard&#8221; to manage the Heroku Scheduler for your app. Add a new job, and set the frequency to **Every 10 minutes**. For your task, enter **curl -I http://your-app-name.herokuapp.com**. This will fetch HTTP response headers from your app, using [Curl][8], every 10 minutes.

It should be noted that method 2 could potentially cause you to have a balance to pay at Heroku. That&#8217;s because Heroku Scheduler has [Dyno Hour Usage][9].

So, there&#8217;s two options that everyone can use to keep your Heroku apps from sleeping, no matter what language your app is written in.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="4608"
					data-ulike-nonce="da0b955744"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_4608"></button><span class="count-box"></span>
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

 [1]: http://heroku.com/
 [2]: https://devcenter.heroku.com/articles/dynos
 [3]: https://devcenter.heroku.com/articles/dynos#dyno-sleeping
 [4]: http://www.uptimerobot.com/
 [5]: http://blog.onemonthrails.com/how-to-fix-the-heroku-30-second-delay/
 [6]: http://www.crowdco.de/tutorials/19
 [7]: https://coderwall.com/p/u0x3nw
 [8]: http://en.wikipedia.org/wiki/CURL
 [9]: https://devcenter.heroku.com/articles/addons-with-dyno-hour-usage
 [10]: #