---
title: Quickly Deploy LAMP Stacks with ServerPilot
author: Tyler Longren
type: post
date: 2014-10-27T13:37:33+00:00
url: /quick-and-easy-lamp-stack-with-serverpilot/
featured_image: /wp-content/uploads/2014/10/serverpilot.png
independent_publisher_primary_category:
  - PHP
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
dsq_thread_id:
  - 3153487179
tags:
  - code
  - composer
  - cool
  - digitalocean
  - gist
  - git
  - GitHub
  - hosting
  - Internet
  - json
  - laravel
  - Linux
  - mysql
  - nginx
  - PHP
  - services
  - tools
  - ubuntu
  - vagrant

---
## Easily Deploy LAMP Stacks, and it&#8217;s free {.subtitle}

I have yet to use [ServerPilot][1], but will be setting up a new [VPS at DigitalOcean][2] in the coming weeks for a new venture. [ServerPilot][1] makes getting a LAMP stack setup very quickly.

[ServerPilot][1] will automatically install **Nginx**, **Apache**, **PHP**, and **MySQL** on _a new, freshly installed/create_d, 64-bit Ubuntu 12.04 or Ubuntu 14.04. So if you&#8217;re using DigitalOcean, create your Droplet, and SSH to it. You should be able to [harden SSH up a little][3], but make sure you don&#8217;t install any new packages yet.

## Getting Started

Getting started with [ServerPilot][1] is crazy easy. All you need to be able to do is SSH into your server and run a command. I _highly_ doubt anyone reading this doesn&#8217;t know how to do this. If you don&#8217;t, [Google will tell you how][4]. 

### 1. Sign Up

[Sign up][1] for a free account with ServerPilot.

### 2. Connect A Server

&#8220;Connect&#8221; a new server. Just enter your servers hostname and click the &#8220;Continue With Setup&#8221; button. Screenshot below.  
[<img loading="lazy" src="https://i1.wp.com/longren.io/wp-content/uploads/2014/10/serverpilot-connect-server.png?resize=920%2C456" alt="serverpilot-connect-server" width="920" height="456" class="aligncenter size-full wp-image-7611" srcset="https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/serverpilot-connect-server.png?w=920&ssl=1 920w, https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/serverpilot-connect-server.png?resize=150%2C74&ssl=1 150w, https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/serverpilot-connect-server.png?resize=300%2C148&ssl=1 300w, https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/serverpilot-connect-server.png?resize=700%2C346&ssl=1 700w" sizes="(max-width: 920px) 100vw, 920px" data-recalc-dims="1" />][5]

### 3. Run The Install

Connect to your server via SSH. Remember, it _must be a new server_, preferably with no additional packages installed yet. To install Nginx, Apache, PHP, and MySQL, run the command below, [from this gist][6]:

<div class="oembed-gist">
  <noscript>
    View the code on <a href="https://gist.github.com/tlongren/37f7379acc48a7cfd3e9">Gist</a>.
  </noscript>
</div>

The `--server-id` and `--server-apikey` values will be provided for you, they&#8217;re blacked out in the screenshot below.  
[<img loading="lazy" src="https://i2.wp.com/longren.io/wp-content/uploads/2014/10/serverpilot.png?resize=957%2C681" alt="serverpilot" width="957" height="681" class="aligncenter size-full wp-image-7614" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/serverpilot.png?w=957&ssl=1 957w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/serverpilot.png?resize=150%2C106&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/serverpilot.png?resize=300%2C213&ssl=1 300w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/serverpilot.png?resize=700%2C498&ssl=1 700w" sizes="(max-width: 957px) 100vw, 957px" data-recalc-dims="1" />][7]

## Additional Information

### On GitHub

ServerPilot also has a GitHub account with two repositories currently. One is [ServerPilot/Vagrantfile][8] and the other is [ServerPilot/API][9].

#### ServerPilot/Vagrantfile

This repository provides a sample [Vagrant][10] configuration for testing ServerPilot. Basically a server that you can use to test ServerPilot before using it on a new, paid VPS. The [README is very detailed][11], definitely read it if you need help using Vagrant. There&#8217;s even an example on using composer to create a Laravel app.

#### ServerPilot/API

From the README, _The ServerPilot API is RESTful and allows you to manage ServerPilot resources using HTTP requests. All responses return JSON objects, including errors._ As seems typical from ServerPilot, the [documentation in the README is excellent][12].

The API will let you do things like list servers, connect new servers, or list all system users, among many others. An example that would list all servers can be seen in the [gist][13] below.

<div class="oembed-gist">
  <noscript>
    View the code on <a href="https://gist.github.com/tlongren/bdcc5bc7dbde7009db02">Gist</a>.
  </noscript>
</div>

That request would return JSON similar to this:

<div class="oembed-gist">
  <noscript>
    View the code on <a href="https://gist.github.com/tlongren/bdcc5bc7dbde7009db02">Gist</a>.
  </noscript>
</div>

<div id="polls-29" class="wp-polls">
</div>

<div id="polls-29-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

### Paid Accounts

You get a pretty cool monitoring dashboard for $10/month. I found the [screenshot below in a post][14] from [Jake Peterson][15], it appears to be the ServerPilot monitoring dashboard.  
[<img loading="lazy" src="https://i1.wp.com/longren.io/wp-content/uploads/2014/10/serverpilot-dashboard-1024x430.jpg?resize=700%2C293" alt="serverpilot-dashboard" width="700" height="293" class="aligncenter size-large wp-image-7622" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/serverpilot-dashboard.jpg?resize=1024%2C430&ssl=1 1024w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/serverpilot-dashboard.jpg?resize=150%2C63&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/serverpilot-dashboard.jpg?resize=300%2C126&ssl=1 300w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/serverpilot-dashboard.jpg?resize=700%2C294&ssl=1 700w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/serverpilot-dashboard.jpg?w=1500&ssl=1 1500w" sizes="(max-width: 700px) 100vw, 700px" data-recalc-dims="1" />][16]  
There&#8217;s the free plan, obviously, and then two paid plans. One is $10/month and the other is $49/month. You can see what you get for your money on their [pricing page][17].

### End

If you&#8217;re a PHP developer and use a VPS provider like [DigitalOcean][2] or [Linode][18], ServerPilot is probably worth checking out. Even if you don&#8217;t end up using, it&#8217;s pretty neat that something like this even exists.

I only have one feature I&#8217;d _really_ like to see, the ability to select certain packages to be installed. If that were included in the $10/month plan, I&#8217;d definitely do it. As it stands currently, though, it&#8217;s definitely a time saver and very well executed. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7609"
					data-ulike-nonce="ef28d814e5"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7609"></button><span class="count-box"></span>
  </div>
</div>

[][19]{.later-button-el}

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

 [1]: https://www.serverpilot.io/?refcode=5d25c4553c95
 [2]: https://www.digitalocean.com/?refcode=cbf49d0481c8
 [3]: https://longren.io/secure-ssh-by-disabling-password-logins/
 [4]: https://www.google.com/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=ssh+vps+digitalocean
 [5]: https://i1.wp.com/longren.io/wp-content/uploads/2014/10/serverpilot-connect-server.png
 [6]: https://gist.github.com/tlongren/37f7379acc48a7cfd3e9
 [7]: https://i2.wp.com/longren.io/wp-content/uploads/2014/10/serverpilot.png
 [8]: https://github.com/ServerPilot/Vagrantfile
 [9]: https://github.com/ServerPilot/API
 [10]: http://www.vagrantup.com/
 [11]: https://github.com/ServerPilot/Vagrantfile/blob/master/README.md
 [12]: https://github.com/ServerPilot/API/blob/master/README.md
 [13]: https://gist.github.com/tlongren/bdcc5bc7dbde7009db02
 [14]: http://digisocialnet.com/blog/serverpilot-vps-server-management
 [15]: http://digisocialnet.com/about
 [16]: https://i1.wp.com/longren.io/wp-content/uploads/2014/10/serverpilot-dashboard.jpg?ssl=1
 [17]: https://serverpilot.io/pricing.html
 [18]: https://www.linode.com/
 [19]: #