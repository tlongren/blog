---
title: Setup Scout Realtime on Ubuntu
author: Tyler Longren
type: post
date: 2014-03-24T13:46:13+00:00
url: /setup-scout-realtime-on-ubuntu/
featured_image: /wp-content/uploads/2014/03/scout-realtime.png
dsq_thread_id:
  - 2492449475
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
independent_publisher_primary_category:
  - Tools
tags:
  - digitalocean
  - GitHub
  - hosting
  - Internet
  - Linux
  - Open Source
  - opensource
  - Personal
  - services
  - tools

---
I love server monitoring. It&#8217;s something I&#8217;ve always liked. When I discovered `top` in about 1998 on Slackware Linux, I fell in love.

Top is old, though. [Scout Realtime][1] isn&#8217;t.

Scout Realtime is built with Ruby and can be installed as a Ruby gem. Make sure you&#8217;ve got **rubygems** installed. If it&#8217;s not installed, then install it.

Scout Realtime doesn&#8217;t work with Ruby 1.8, it requires Ruby 1.9. Installing Ruby 1.9 is [pretty easy and is explained in detail in this post][2].

## Install Scout Realtime

This has been tested on Ubuntu 13.10 on a [DigitalOcean VPS][3]. 

Now you can install Scout Realtime:  
<span class="lang:sh decode:true  crayon-inline " >sudo gem install scout_realtime</span>

After it&#8217;s been installed, launch it! You can run it as root or as your normal user. If you want to run it as root, just add `sudo` before the `scout_realtime` command below.  
<span class="lang:sh decode:true  crayon-inline " >scout_realtime</span>

That&#8217;ll start Scout Realtime on it&#8217;s default listening port, which is 5555. If you&#8217;d like it to run on a different port, run `scout_realtime --help` to see how to go about that.

## Access Scout Realtime

There&#8217;s a couple ways that you can access Scout Realtime in your browser.

The quickest and safest way is to setup a [SSH tunnel][4]. This is how [Scout shows Realtime being setup][1].  
<span class="lang:sh decode:true  crayon-inline " >ssh -NL 5555:localhost:5555 user@ip_or_hostname</span> 

Replace `user@ip_or_hostname` with your SSH user and hostname.

Once the SSH tunnel is setup and running, open up your web browser and navigate to `http://localhost:5555`. You should see Scout Realtime, it&#8217;ll look similar to the screenshot that&#8217;s attached to this post.

You can also open a firewall port, allowing access to port 5555, or whatever port you&#8217;ve got Scout Realtime running on. Doing this will provide you with persistent access to Scout Realtime. Just navigate to your IP address or domain on the relevant port.

That&#8217;s it! Scout Realtime should now be running on your server, and you&#8217;ve got a couple of different options for accessing Scout Realtime.

For more on Scout Realtime, [visit the site][5] or [view the source code on GitHub][5]. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="6218"
					data-ulike-nonce="b5d156d597"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_6218"></button><span class="count-box"></span>
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

 [1]: http://scoutapp.github.io/scout_realtime/
 [2]: http://leonard.io/blog/2012/05/installing-ruby-1-9-3-on-ubuntu-12-04-precise-pengolin/
 [3]: https://www.digitalocean.com/?refcode=cbf49d0481c8
 [4]: http://www.engadget.com/2006/03/21/how-to-ssh-tunnels-for-secure-network-access/
 [5]: https://github.com/scoutapp/scout_realtime
 [6]: #