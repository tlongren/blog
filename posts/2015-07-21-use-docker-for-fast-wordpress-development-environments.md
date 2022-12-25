---
title: Use Docker for Fast WordPress Development Environments
author: Tyler Longren
type: post
date: 2015-07-21T06:42:44+00:00
url: /use-docker-for-fast-wordpress-development-environments/
featured_image: /wp-content/uploads/2015/07/docker.png
independent_publisher_primary_category:
  - WordPress
dsq_thread_id:
  - 3955061703
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cool
  - GitHub
  - Internet
  - Linux
  - Open Source
  - Personal
  - PHP
  - poll
  - tools
  - WordPress

---
## A Dockerfile That Provides Quick WordPress Development Environments

Back in May of this year I started playing around with Docker quite a bit. Took me a bit to wrap my brain around everything Docker can do, wish I had [read this article][1] from Adam Ierymenko before starting.

Anyway, Docker describes itself as such:

<blockquote class="wp-block-quote">
  <p>
    Docker is an open platform for building, shipping and running distributed applications. It gives programmers, development teams and operations engineers the common toolbox they need to take advantage of the distributed and networked nature of modern applications.
  </p>
</blockquote>

I&#8217;m not using Docker to it&#8217;s fullest extent, not even close. I mostly use it for setting up quick WordPress development environments for building client sites or just to do some testing.

I came across an outdated Dockerfile that had exactly what I needed but lacked the ability to SSH to the Docker container. I [forked it on GitHub][2] and added some modifications (like SSH).

It&#8217;s on the [Docker Hub Registry][3], making it super easy to use. There&#8217;s a few items on the to-do list, but the one I want to take care of first is adding support for [Docker Compose][4], which will make installation even easier.

To get started with this Docker image, you just need to [have Docker installed][5] and then run the following command:

<pre class="wp-block-preformatted">sudo docker pull tlongren/docker-wordpress-nginx-ssh:latest</pre>

Once you&#8217;ve got the Docker image pulled, fire up a new container like with the command below. It will create a new Docker container named _project-name_.

<pre class="wp-block-preformatted">sudo docker run -p 80:80 -p 2222:22 --name project-name -d tlongren/docker-wordpress-nginx-ssh:latest</pre>

Give it a bit to get everything setup then navigate to _http://127.0.0.1:80_ in your browser to access your new WordPress install.

For more information I suggest [checking out the readme][3]. Every time that I push commits to GitHub, a new build of the Docker image will automatically be built as I&#8217;ve got it setup as an automated build repository at the Docker Hub Registry. Pretty nifty.

So, I&#8217;m relatively new to Docker, if you&#8217;re a pro and see something I should be doing differently, please let me know. Any advice on setting up Docker Compose for this project would be great, too (if I&#8217;m not mistaken, it just involved linking multiple containers together).

<div id="polls-32" class="wp-polls">
</div>

<div id="polls-32-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="8089"
					data-ulike-nonce="da97ec8d38"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image image-unlike wp_ulike_btn_is_active wp_likethis_8089"></button><span class="count-box">8+</span>
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

 [1]: http://adamierymenko.com/docker-not-even-a-linker/
 [2]: https://github.com/tlongren/docker-wordpress-nginx-ssh/
 [3]: https://registry.hub.docker.com/u/tlongren/docker-wordpress-nginx-ssh/
 [4]: https://docs.docker.com/compose/
 [5]: http://docs.docker.com/mac/started/
 [6]: #