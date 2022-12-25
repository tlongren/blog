---
title: Quick and Easy Remote Backups
author: Tyler Longren
type: post
date: 2005-07-09T22:06:54+00:00
url: /quick-and-easy-remote-backups/
views:
  - 3232
DiggURL:
  - http://digg.com/software/Quick_and_Easy_Offsite_Backups
dsq_thread_id:
  - 1385909271
independent_publisher_primary_category:
  - Internet
tags:
  - backup
  - code
  - Linux
  - programming
  - scripts

---
 

I backup my database, website, and my home directory on a daily basis to a remote server via [SSH][1] and [rsync][2]. Rsync is a tool that synchronizes directories. I also use it for grabbing current copies of slackware-10.1 and slackware-current.

It&#8217;s really easy to backup files to a remote server with these tools. I create tar archives of my needed directories and store the current ones in /opt/backups. I&#8217;ve made various bash scripts to do this on a daily basis for me automatically. After that&#8217;s complete, the code shown below is run. It transfers my /opt/backups directory to the remote server. It&#8217;s path on the remote server would be /home/tyler/backups. All you need to do is set the SERVER variable to the hostname of the server you&#8217;re backing up to.  
<figure class="wp-block-embed is-type-rich is-provider-embed-handler">

<div class="wp-block-embed__wrapper">
  <div class="oembed-gist">
    <noscript>
      View the code on <a href="https://gist.github.com/tlongren/ad8992557c0b260a88795accfe9be8e5">Gist</a>.
    </noscript>
  </div>
</div></figure> 

The hardest part is finding a remote server that you&#8217;re able to backup to. If you&#8217;re lucky, your web host will allow you SSH access. There&#8217;s no need for the server end to have rsync installed. All it needs is SSH. I know [BlueHost][3] gives account holders SSH access. They&#8217;ve been hosting our sites at work for a while now and promptly gave me an SSH account. Their sites said they&#8217;d need an ID, but they didn&#8217;t require one from me for one reason or another. I backup to a freinds Linux box that&#8217;s located in a datacenter somewhere.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="1943"
					data-ulike-nonce="e9fd7875b1"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_1943"></button><span class="count-box">1+</span>
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

 [1]: http://www.openssh.com/
 [2]: http://samba.anu.edu.au/rsync/
 [3]: http://www.bluehost.com/
 [4]: #