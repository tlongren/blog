---
title: Record Speedtest.net Results From the Command Line
author: Tyler Longren
type: post
date: 2014-03-03T17:05:46+00:00
url: /log-speedtest-net-results-from-the-command-line/
featured_image: /wp-content/uploads/2014/03/speedtest-cli-crushed.png
dsq_thread_id:
  - 2328798055
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - bash
  - digital ocean
  - digitalocean
  - git
  - GitHub
  - Internet
  - Linux
  - Open Source
  - Personal
  - tutorials

---
## For those who live in the command line as much as possible {.subtitle}

### Install speedtest-cli

[speedtest-cli][1] is a Python app that provides a command line interface for testing bandwidth using [speedtest.net][2]. Installation is simple. It should work on Linux and OS X.

### The Bash Scripts

There&#8217;s two scripts, `speedtest.sh` and `speedtest-simple.sh`. Pretty self-explanatory. Results from `speedtest.sh` are stored in **st_results** in the current working directory. `speedtest-simple.sh` results are stored in **st\_results\_simple**, also in the current working directory.

<div class="oembed-gist">
  <noscript>
    View the code on <a href="https://gist.github.com/tlongren/9245891">Gist</a>.
  </noscript>
</div>

### speedtest.sh Results

Below are the results of two speedtests run with `speedtest.sh`, along with the sharing image URL.

> Retrieving speedtest.net configuration&#8230;  
> Retrieving speedtest.net server list&#8230;  
> Testing from Mediacom Communications (173.22.40.33)&#8230;  
> Selecting best server based on ping&#8230;  
> Hosted by CHRJO (Council Bluffs, IA) [204.50 km]: 20.981 ms  
> Testing download speed&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;.  
> Download: 32.44 Mbit/s  
> Testing upload speed&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;..  
> Upload: 5.57 Mbit/s  
> Share results: http://www.speedtest.net/result/3335225265.png .  
> #############
> 
> Retrieving speedtest.net configuration&#8230;  
> Retrieving speedtest.net server list&#8230;  
> Testing from Mediacom Communications (173.22.40.33)&#8230;  
> Selecting best server based on ping&#8230;  
> Hosted by American Broadband (Blair, NE) [213.79 km]: 20.981 ms  
> Testing download speed&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;.  
> Download: 33.03 Mbit/s  
> Testing upload speed&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;&#8230;..  
> Upload: 5.49 Mbit/s  
> Share results: http://www.speedtest.net/result/3335230578.png .  
> #############

You can get less verbose output by modifying the `speedtest-cli` flags. `speedtest-cli --simple --share` will produce very simple results that are a bit easier to read. Two tests with the `speedtest-simple.sh` script are below. Note the absolute crap speeds. Wonderful hotel wi-fi, hah!

### speedtest-simple.sh Results

> Ping: 13.351 ms  
> Download: 1.92 Mbit/s  
> Upload: 0.94 Mbit/s  
> Share results: http://www.speedtest.net/result/3342143070.png .  
> #############
> 
> Ping: 13.431 ms  
> Download: 1.80 Mbit/s  
> Upload: 0.93 Mbit/s  
> Share results: http://www.speedtest.net/result/3342149985.png .  
> #############

It&#8217;s a very, very simple way of logging the speedtest.net results, but it&#8217;ll do for most situations. When I get some free time this week, I&#8217;m going to combine `speedtest.sh` and `speedtest-simple.sh` and make it accept a `--simple` argument to generate the simple log.

After that&#8217;s done, I&#8217;ll be dropping the results into a SQLite database. I&#8217;ve gotten pretty familiar with SQLite lately, so it shouldn&#8217;t be too difficult.

Once this stuff is logging to a SQLite databse, I&#8217;ll put it up on GitHub, I can&#8217;t be the only one who would love to run SQL queries against this sort of personalized bandwidth data.

**Update April 19, 2014:** [Updated the code in the GitHub Gist to include the date and time][3] of the speedtest. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5517"
					data-ulike-nonce="134eae912e"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5517"></button><span class="count-box">1+</span>
  </div>
</div>

[][4]{.later-button-el}

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

 [1]: https://github.com/sivel/speedtest-cli
 [2]: http://speedtest.net/
 [3]: https://gist.github.com/tlongren/9245891
 [4]: #