---
title: 'Find Shellshock Exploit Attempts & Probes From the Command Line and Papertrail'
author: Tyler Longren
type: post
date: 2014-10-23T11:05:22+00:00
url: /find-shellshock-attempts-probes-with-papertrail/
featured_image: /wp-content/uploads/2014/10/bash.png
independent_publisher_primary_category:
  - Security
dsq_thread_id:
  - 3145510186
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cloudflare
  - cool
  - digitalocean
  - fucked
  - git
  - GitHub
  - hosting
  - Internet
  - papertrail
  - Personal
  - Security
  - services
  - shellshock
  - tools

---
## Never hurts to make sure {.subtitle}

I&#8217;ve [written][1] [about][2] [Papertrail][3] a [few][4] times before, I love the service and it&#8217;s just too valuable to _not_ use.

[Papertrail][3] makes it super easy to find Shellshock exploit attempts and probes. Probes are just checking a machine to see if it&#8217;s vulnerable to Shellshock. If you&#8217;re using CloudFlare, you&#8217;ll never see any Shellshock attempts show up in your logs, [CloudFlare doesn&#8217;t even let them through][5].

### See If Shellshock Affects You

Checking to see if your system is vulnerable to Shellshock is quite easy. It takes a relatively simple bash command:

<pre class="lang:sh decode:true " >env x='() { :;}; echo vulnerable to shellshock' bash -c "echo All good"</pre>

Run that code in a terminal. If you see `All good`, you&#8217;re not vulnerable. However, if you see `vulnerable to shellshock`, you are potentially vulnerable.

[<img loading="lazy" src="https://i1.wp.com/longren.io/wp-content/uploads/2014/10/Yahoo-WinZip-Servers-Shellshock-Bug.jpg?resize=630%2C354" alt="Yahoo-WinZip-Servers-Shellshock-Bug" width="630" height="354" class="aligncenter size-full wp-image-7575" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/Yahoo-WinZip-Servers-Shellshock-Bug.jpg?w=630&ssl=1 630w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/Yahoo-WinZip-Servers-Shellshock-Bug.jpg?resize=150%2C84&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/Yahoo-WinZip-Servers-Shellshock-Bug.jpg?resize=300%2C168&ssl=1 300w" sizes="(max-width: 630px) 100vw, 630px" data-recalc-dims="1" />][6]

[Shellshocker.net][7] provides a script that will download, compile, and install the newest version of bash for you. You should only use it though if your Linux distribution hasn&#8217;t already provided updated security release packages. If you&#8217;re interested, the code that runs Shellshocker.net is [available on GitHub][8].

### Find Shellshock Attemps and Probes Via The Command Line

This is very easy as long as you know the location of your Apache access log file. It&#8217;s typically something like `/var/log/apache2/access.log`. Assuming that&#8217;s the location of your Apache access log file, this command will pull out all the Shellshock probes and attempts:

<pre class="lang:sh decode:true " >grep '() {' /var/log/apache2/access.log</pre>

If nothing was returned, that means nobody has been trying to exploit Shellshock on your system, or even checking to see if your system is susceptible to Shellshock. If results are returned, look them over carefully to examine where the attempts are coming from, an IP address will be associated with every attempt.

#### Shellshocker.net Checker

[Shellshocker.net][7] also provides a [bash script to check your machines][9] for the Shellshock vulnerability. You can download the script and run it manually from your terminal, or, if you have cURL installed, run the following command:

<pre class="lang:sh decode:true " >curl https://shellshocker.net/shellshock_test.sh | bash</pre>

Running that command will produce results similar to the screenshot seen below. It checks for a number of Shellshock related vulnerabilities.  
[<img loading="lazy" src="https://i2.wp.com/longren.io/wp-content/uploads/2014/10/shellshocker.png?resize=736%2C443" alt="shellshocker" width="736" height="443" class="aligncenter size-full wp-image-7581" srcset="https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/shellshocker.png?w=736&ssl=1 736w, https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/shellshocker.png?resize=150%2C90&ssl=1 150w, https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/shellshocker.png?resize=300%2C180&ssl=1 300w, https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/shellshocker.png?resize=700%2C421&ssl=1 700w" sizes="(max-width: 736px) 100vw, 736px" data-recalc-dims="1" />][10]

### Find Shellshock Attemps and Probes With Papertrail

Go to your Papertrail events tab and search for the following:  
`"() {"`

If anything is returned, those are Shellshock probes. Some example probes are listed in the [gist that&#8217;s embedded below][11]. None of the offending IP addresses have been redacted.

<div class="oembed-gist">
  <noscript>
    View the code on <a href="https://gist.github.com/tlongren/ea2ca1a0bd1b5b1ec3be">Gist</a>.
  </noscript>
</div>

These actually made it through to Papertrail, which shouldn&#8217;t happen since longren.io sits behind Cloudflare. I&#8217;ll open a support ticket with them about it and update this post later. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7518"
					data-ulike-nonce="58b94d5ec1"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7518"></button><span class="count-box"></span>
  </div>
</div>

[][12]{.later-button-el}

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

 [1]: https://longren.io/monitor-sshd-events-with-papertrail/
 [2]: https://longren.io/receive-alerts-on-ssh-or-sftp-logins-with-papertrail/
 [3]: https://papertrailapp.com/?thank=33d541
 [4]: https://longren.io/aggregate-system-and-application-logs-with-papertrail/
 [5]: https://blog.cloudflare.com/shellshock-protection-enabled-for-all-customers/
 [6]: https://i1.wp.com/longren.io/wp-content/uploads/2014/10/Yahoo-WinZip-Servers-Shellshock-Bug.jpg
 [7]: https://shellshocker.net/
 [8]: https://github.com/wreiske/shellshocker
 [9]: https://github.com/wreiske/shellshocker/blob/master/shellshock_test.sh
 [10]: https://i2.wp.com/longren.io/wp-content/uploads/2014/10/shellshocker.png
 [11]: https://gist.github.com/tlongren/ea2ca1a0bd1b5b1ec3be
 [12]: #