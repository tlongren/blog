---
title: Introducing Kegplan.io
author: Tyler Longren
type: post
date: 2013-12-08T04:05:53+00:00
url: /introducing-kegplan-io/
featured_image: /wp-content/uploads/2013/12/kegplan.png
dsq_thread_id:
  - 2034348560
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - digital ocean
  - git
  - heroku
  - Internet
  - kegplan.io
  - Linux
  - Open Source
  - paas
  - Personal
  - PHP
  - saas
  - Work

---
I recently made a [post over at the VPSstat.us blog][1] just letting folks know what&#8217;s going on and why there&#8217;s bee such a delay in getting our product out there for everyone to use. Rather than go into that again, just checkout the post at the VPSstat.us Blog.

The gist of it is, a friend and I have been working on a new startup idea. [Kegplan.io][2], a SaaS business that helps liquor stores to better manage their kegs, with many additional features in the pipeline. Ace (the friend), who runs I-35 Spirits in Ankeny, IA, was the inspiration for the idea. Managing kegs, such as pick up dates, return dates, weather or not the customer needs a tapper, etc, can be a real time drain. Most liquor store owners have much, much better things they could be doing.

We&#8217;re almost ready to release a private beta and invite some local liquor stores to try it out. &#8220;Local&#8221; being in Iowa, Central Iowa preferably, but that doesn&#8217;t mean we won&#8217;t leave Iowa if we can get a few potential customers lined up out of state.

There&#8217;s a very, very basic homepage up now at <http://kegplan.io>. Please forgive me for it&#8217;s ugliness, most of my time so far has been spent developing the software that&#8217;s installed on customer sites. I&#8217;ll be hitting kegplan.io pretty hard in the next few weeks, including incorporating [Pure CSS][3] to make development a bit faster, and also provide full responsiveness.

Below is an overview of how to integrate kegplan.io into your website:

  1. Signup for a kegplan.io account
  2. Choose a plan (beta will be totally free, no cc details required)
  3. Choose the keg beers that your store has available from our admin interface, or send us a spreadsheet and we&#8217;ll import it just for you
  4. Install our script on the page on your site you&#8217;d like to have the keg request form
  5. That&#8217;s it! Direct customers to the page you installed the script on and they&#8217;ll be able to submit keg requests. Requests are sent to your email and also stored in a database so you can have all sorts of neat reports and graphs.

Since this is a service that can immediately have a positive impact on businesses, and a friends business specifically, I&#8217;m focusing on getting [kegplan.io][4] launched before putting more work into [VPSstat.us][5]. Kegplan is a relatively simple piece of software so getting it production ready shouldn&#8217;t take more than a couple of weeks.

All the scripts that are installed on customer websites are hosted on [Heroku][6] for maximum availability. The customer control panel is hosted on [a pretty beefy VPS from DigitalOcean][7]. We may eventually switch to using DigitalOcean&#8217;s private networking with a few different VPS&#8217;s in different locations, but I have a feeling Heroku will be plenty sufficient.

Shortly before the private beta release, we&#8217;ll be integrating kegplan.io into [i35spirits.com][8]. Once it&#8217;s been thoroughly tested on i35spirits.com, we&#8217;ll drop the private beta. If you&#8217;re interested in more info or if you want to get in the private beta right away, email me (Tyler) at `tyler at kegplan dot io`.

If you&#8217;ve got any suggestions on the best, most secure way to deliver scripts for installation on third-party websites, I&#8217;d love to hear your thoughts. Right now I&#8217;m including a script on customer sites that&#8217;s delivered via HTTPS, and basically prints the form on the customer website. And I&#8217;m using jQuery and AJAX to send the results back to an SSL enabled domain for storage in a database and to send the necessary notification emails.

Anyway, keep checking [kegplan.io][2] for updates. There&#8217;ll be a official kegplan.io blog eventually, but right now all announcements will be made here at longren.org, and maybe at the [I-35 Spirits website][9].

Would love to hear any comments. If you know anyone who runs a liquor store or other establishment that sells kegs, please tell them about us! We&#8217;re new at this too, so we&#8217;ll be helping beta users through every step of the on-boarding process.

Please bear with us as we finish out the customer-facing <http://kegplan.io> website. I don&#8217;t have a lot of time to work on it, other than nights and some weekends, but there&#8217;s not a _whole_ lot to do. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="4804"
					data-ulike-nonce="1757a05fa7"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_4804"></button><span class="count-box"></span>
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

 [1]: http://blog.vpsstat.us/posts/were-still-here
 [2]: http://kegplan.io
 [3]: http://purecss.io/
 [4]: http://kegplan.io/
 [5]: http://blog.vpsstat.us/
 [6]: http://www.heroku.com
 [7]: https://www.digitalocean.com/?refcode=cbf49d0481c8
 [8]: http://dev.i35spirits.com/
 [9]: http://dev.i35spirits.com
 [10]: #