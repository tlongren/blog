---
title: 'Scotch Box: A Vagrant LAMP Stack That Just Works'
author: Tyler Longren
type: post
date: 2014-10-20T12:42:19+00:00
url: /scotch-box-a-vagrant-lamp-stack-that-just-works/
featured_image: /wp-content/uploads/2014/10/scotchbox.png
independent_publisher_primary_category:
  - PHP
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
dsq_thread_id:
  - 3134152600
tags:
  - cool
  - digitalocean
  - framework
  - git
  - GitHub
  - hosting
  - Internet
  - Linux
  - Open Source
  - Personal
  - PHP
  - services
  - tools
  - vagrant
  - Work

---
## Just a dead-simple local Vagrant LAMP stack for developers {.subtitle}

I discovered [Scotch Box][1] recently, brought to us by the folks at [scotch.io][2]. It actually looks like [Nicholas Cerminara][3] has done most of the work, or as least done all of the [committing to GitHub][4]. Here&#8217;s the [Scotch Box announcement at the Scotch.io blog][5].

After using Scotch Box for a day, I&#8217;ve decided this is how I will do all future development work. It&#8217;s so easy, and you really don&#8217;t need to know much about [Vagrant][6] or VirtualBox to get up and running with Scotch Box.

[Scotch Box][1] has a [repository setup at GitHub][7] that explains how to make use of Scotch Box. Basically, just clone the repository, and then run `vagrant up` inside that repo.

Scotch Box is currently running Ubuntu 12.04.5. Here&#8217;s a bit from the Scotch Box readme:

<blockquote class="wp-block-quote">
  <p>
    Scotch Box is a preconfigured Vagrant Box with a full array of LAMP Stack features to get you up and running with <a href="https://www.vagrantup.com/">Vagrant</a> in no time.
  </p>
  
  <p>
    A lot of PHP websites and applications don’t require much server configuration or overhead at first. This box should have all your needs for doing basic development so you don’t have to worry about configuring Vagrant and you can simply focus on your code.
  </p>
  
  <p>
    No provisioning tools or setup is really even required with Scotch Box. Since everything is packaged into the box, running “vagrant” is super fast, you’ll never have to worry about your environment breaking with updates, and you won’t need Internet to code.
  </p>
</blockquote>

<div id="polls-29" class="wp-polls">
</div>

<div id="polls-29-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

### Bringing Scotch Box Up

<div class="wp-block-image">
  <figure class="aligncenter"><a href="https://i1.wp.com/longren.io/wp-content/uploads/2014/10/scotch.jpg"><img loading="lazy" width="900" height="698" src="https://i1.wp.com/longren.io/wp-content/uploads/2014/10/scotch.jpg?resize=900%2C698" alt="scotch" class="wp-image-7557" srcset="https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/scotch.jpg?w=900&ssl=1 900w, https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/scotch.jpg?resize=150%2C116&ssl=1 150w, https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/scotch.jpg?resize=300%2C232&ssl=1 300w, https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/scotch.jpg?resize=700%2C542&ssl=1 700w" sizes="(max-width: 900px) 100vw, 900px" data-recalc-dims="1" /></a></figure>
</div>

Once you&#8217;ve run `vagrant up`, you&#8217;ll be able to access your site at <http://192.168.33.10/>, you should see something similar to the image below.  


### Useful Stuff in Scotch Box

  * PHP 5.5
  * No Internet connection required
  * PHP errors turned on
  * Laravel and WordPress ready (and others)
  * Operating System agnostic
  * Goodbye XAMPP / WAMP
  * New Vagrant version? Update worry free. ScotchBox is very reliable with a lesser chance of breaking with various updates
  * Bootstrap and jQuery are saved in the server&#8217;s home folder in case you don&#8217;t have Internet (usually plains, trains or cars)
  * Chef and Puppet ready in case you want to add extra features on Vagrant Up
  * Super easy database access and control  
    MIT License

### Server Components Included

  * Apache
  * Vim
  * MySQL
  * PHP 5.5
  * Git
  * Screen
  * Composer
  * cURL
  * GD and Imagick
  * Mcrypt
  * Memcache and Memcached

### Front End Stuff Included

  * NPM
  * Grunt
  * Bower
  * Yeoman
  * Gulp

<div class="wp-block-image">
  <figure class="aligncenter"><a href="https://i2.wp.com/longren.io/wp-content/uploads/2014/10/vagrant-ssh.jpg"><img loading="lazy" width="900" height="613" src="https://i2.wp.com/longren.io/wp-content/uploads/2014/10/vagrant-ssh.jpg?resize=900%2C613" alt="vagrant-ssh" class="wp-image-7562" srcset="https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/vagrant-ssh.jpg?w=900&ssl=1 900w, https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/vagrant-ssh.jpg?resize=150%2C102&ssl=1 150w, https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/vagrant-ssh.jpg?resize=300%2C204&ssl=1 300w, https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/vagrant-ssh.jpg?resize=700%2C476&ssl=1 700w" sizes="(max-width: 900px) 100vw, 900px" data-recalc-dims="1" /></a></figure>
</div>

You can SSH to your server as well, by running `vagrant ssh`. Upon logging in via SSH you&#8217;ll see something similar to the image below.  


Scotch Box is in its infancy still. It&#8217;s [initial commit to GitHub was on October 6, 2014][8] and has about 10 commits in total.

Updating Scotch Box is easy too. To check for an updated version with Vagrant, do `vagrant box outdated`. That will tell you if there&#8217;s a newer version available. If there is a newer version available, you can update to it by running `vagrant box update`.

Head to the official Scotch Box website for more information on setting up databases, setting a hostname, and for more details on updating the box. Some basic Vagrant commands are also included to help you with basic Vagrant usage (ie: pausing, resuming, or destroying a server).

If you&#8217;re a LAMP developer like I am, and are tired of developing on your client&#8217;s dev servers, [Scotch Box][1] could be a good solution for you to develop locally. It&#8217;s sometimes much easier to develop locally then having to rely on a slow dev server provided by your client. `:)`

<div class="wp-block-jetpack-tiled-gallery aligncenter is-style-rectangular">
  <div class="tiled-gallery__gallery">
    <div class="tiled-gallery__row">
      <div class="tiled-gallery__col">
        <figure class="tiled-gallery__item"><img srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/vagrant-ssh.jpg?strip=info&#038;w=600&#038;ssl=1 600w,https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/vagrant-ssh.jpg?strip=info&#038;w=900&#038;ssl=1 900w" alt="" aria-label="image 1 of 3 in gallery" data-height="613" data-id="7562" data-link="https://www.longren.io/scotch-box-a-vagrant-lamp-stack-that-just-works/vagrant-ssh/" data-url="https://www.longren.io/wp-content/uploads/2014/10/vagrant-ssh.jpg" data-width="900" src="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/vagrant-ssh.jpg?ssl=1" /></figure>
      </div>
      
      <div class="tiled-gallery__col">
        <figure class="tiled-gallery__item"><img srcset="https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/scotch.jpg?strip=info&#038;w=600&#038;ssl=1 600w,https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/scotch.jpg?strip=info&#038;w=900&#038;ssl=1 900w" alt="" aria-label="image 2 of 3 in gallery" data-height="698" data-id="7557" data-link="https://www.longren.io/scotch-box-a-vagrant-lamp-stack-that-just-works/scotch/" data-url="https://www.longren.io/wp-content/uploads/2014/10/scotch.jpg" data-width="900" src="https://i2.wp.com/www.longren.io/wp-content/uploads/2014/10/scotch.jpg?ssl=1" /></figure>
      </div>
      
      <div class="tiled-gallery__col">
        <figure class="tiled-gallery__item"><img srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/scotchbox-1024x483.png?strip=info&#038;w=600&#038;ssl=1 600w,https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/scotchbox-1024x483.png?strip=info&#038;w=900&#038;ssl=1 900w,https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/scotchbox-1024x483.png?strip=info&#038;w=1200&#038;ssl=1 1200w,https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/scotchbox-1024x483.png?strip=info&#038;w=1500&#038;ssl=1 1500w,https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/scotchbox-1024x483.png?strip=info&#038;w=1800&#038;ssl=1 1800w,https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/scotchbox-1024x483.png?strip=info&#038;w=1902&#038;ssl=1 1902w" alt="" aria-label="image 3 of 3 in gallery" data-height="898" data-id="7553" data-link="https://www.longren.io/scotch-box-a-vagrant-lamp-stack-that-just-works/scotchbox/" data-url="https://www.longren.io/wp-content/uploads/2014/10/scotchbox-1024x483.png" data-width="1902" src="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/10/scotchbox-1024x483.png?ssl=1" /></figure>
      </div>
    </div>
  </div>
</div>

All the images in this post are included in the gallery below.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7552"
					data-ulike-nonce="7495b4dcc2"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7552"></button><span class="count-box"></span>
  </div>
</div>

[][9]{.later-button-el}

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

 [1]: http://box.scotch.io/
 [2]: http://scotch.io
 [3]: https://github.com/ncerminara
 [4]: https://github.com/scotch-io/scotch-box/commits/master
 [5]: http://scotch.io/bar-talk/introducing-scotch-box-a-vagrant-lamp-stack-that-just-works
 [6]: https://www.vagrantup.com/
 [7]: https://github.com/scotch-io/scotch-box
 [8]: https://github.com/scotch-io/scotch-box/commit/4a4025b9ace71fd82c4061588ded004bf3d72503
 [9]: #