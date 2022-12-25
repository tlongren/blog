---
title: Install Tarsnap On a DigitalOcean VPS or Any Ubuntu 14.04 or Newer System
author: Tyler Longren
type: post
date: 2014-08-05T13:27:08+00:00
url: /install-tarsnap-on-a-digitalocean-vps-or-any-ubuntu-14-04-or-newer-system/
featured_image: /wp-content/uploads/2014/08/tarsnap.png
independent_publisher_primary_category:
  - Services
dsq_thread_id:
  - 2901754438
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cool
  - digitalocean
  - hosting
  - Internet
  - Linux
  - Personal
  - Security
  - services
  - tools

---
## Securely and remotely backup your server using Tarsnap {.subtitle}

[Tarsnap][1] is a great service. It&#8217;s extremely affordable and secure. I mentioned it briefly in [my previous post about MySQL backups][2].

Tarsnap is only $0.25 / GB-month for storage and $0.25 / GB for bandwidth, which is extremely affordable. You can add funds to your account whenever you like, which is also very nice. Your initial fund deposit must be at least $5. You can [signup for a Tarsnap account here][3].

Installing it on a stock Ubuntu 14.04 LTS installation requires some additional steps to get everything working nicely.

### 1. Install dependencies

<pre class="lang:sh decode:true " >sudo apt-get install build-essential ext2fs-dev zlib1g-dev libssl-dev </pre>

### 2. Install Tarsnap

[Download Tarsnap][4], I do it like this with wget:

<pre class="lang:sh decode:true " >wget --no-check-certificate https://www.tarsnap.com/download/tarsnap-autoconf-1.0.35.tgz</pre>

Now we need to extract, configure, and compile Tarsnap.

<pre class="lang:sh decode:true " >tar xfz tarsnap-autoconf-1.0.35.tgz
cd tarsnap-autoconf-1.0.35
./configure
sudo make install clean</pre>

### 3. Configure Tarsnap

First, copy the example config to the live config:

<pre class="lang:sh decode:true " >sudo mv /usr/local/etc/tarsnap.conf.sample /usr/local/etc/tarsnap.conf</pre>

If you receive an error with that command, like `mkdir: cannot create directory` , ignore it and continue on.

Next, we need to generate a tarsnap key for your machine. I like to keep my tarsnap key in my home directory, so I run something like this:

<pre class="lang:sh decode:true " >mkdir ~/.tarsnap
tarsnap-keygen --keyfile /home/youruser/.tarsnap/tarsnap.key --user your@email.com --machine your-machine-name</pre>

You&#8217;ll be prompted for your Tarsnap password when running `tarsnap-keygen`.

Now, edit the `tarsnap.conf` file:

<pre class="lang:sh decode:true " >sudo pico /usr/local/etc/tarsnap.conf</pre>

Point the _keyfile_ directive to the key file we created a couple steps ago. The top of your tarsnap.conf file should look similar to this now:

<pre class="lang:sh decode:true " >### Recommended options

# Tarsnap cache directory
cachedir /tmp/tarsnap-cache

# Tarsnap key file
keyfile /home/youruser/.tarsnap/tarsnap.key</pre>

### 4. Use Tarsnap to Make a Backup

You&#8217;ll want get familiar with the [Tarsnap manpages][5]. To create your first archive, with a name of _servername-20140805_, do this:

<pre class="lang:sh decode:true " >tarsnap -c -f servername-20140805 /home/youruser</pre>

That will backup the _/home/youruser_ folder to Tarsnap! Depending on the size of the backup and speed of your connection, it could take quite some time to finish the backup.

Below is the output of tarsnap &#8211;help, if you&#8217;re interested.  
[<img loading="lazy" src="https://i0.wp.com/longren.io/wp-content/uploads/2014/08/tarsnap-help.png?resize=952%2C503" alt="tarsnap-help" width="952" height="503" class="aligncenter size-full wp-image-7320" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/08/tarsnap-help.png?w=952&ssl=1 952w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/08/tarsnap-help.png?resize=150%2C79&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/08/tarsnap-help.png?resize=300%2C158&ssl=1 300w" sizes="(max-width: 952px) 100vw, 952px" data-recalc-dims="1" />][6]

You can read [more about Tarsnap at their homepage, tarsnap.com][1]. They also have a [page describing their infrastructure setup][7], which is kinda neat. [Tarsnap][1] also [runs a bug bounty program][8].

I&#8217;ve only tested this on [DigitalOcean VPS&#8217;s running Ubuntu 14.04 x64][9], but it should work on most Ubuntu variants.

Did I miss something or get something totally wrong? If so, please let me know, the comments are open! 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7318"
					data-ulike-nonce="5925984231"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7318"></button><span class="count-box"></span>
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

 [1]: https://tarsnap.com/
 [2]: http://longren.io/backup-and-compress-mysql-in-one-command/
 [3]: https://www.tarsnap.com/account.html
 [4]: https://www.tarsnap.com/download.html
 [5]: http://www.tarsnap.com/man.html
 [6]: https://i0.wp.com/longren.io/wp-content/uploads/2014/08/tarsnap-help.png
 [7]: https://www.tarsnap.com/infrastructure.html
 [8]: https://www.tarsnap.com/bugbounty.html
 [9]: https://www.digitalocean.com/?refcode=cbf49d0481c8
 [10]: #