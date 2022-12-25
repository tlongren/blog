---
title: Backup and Compress a MySQL Database With One Command
author: Tyler Longren
type: post
date: 2014-08-04T12:45:30+00:00
url: /backup-and-compress-mysql-in-one-command/
featured_image: /wp-content/uploads/2014/08/backup_mysql.png
independent_publisher_primary_category:
  - Linux
dsq_thread_id:
  - 2898906065
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - backup
  - bash
  - cool
  - hosting
  - Internet
  - Linux
  - Personal
  - rsync
  - Security
  - services
  - tutorials

---
 

## I&#8217;ll show you how to restore the backup, too!

I like to use simple bash scripts to do various tasks. Backing up MySQL is one of them.

I recently decided to start compressing my MySQL backups, as I started including all databases in one fell swoop. I use [bzip2][1] to compress the `.sql` files produced by [mysqldump][2]. [bzip2 is standard][3] on pretty much every *nix operating system, so you likely won&#8217;t need to install it.

I&#8217;m also using [Tarsnap][4] for backups now, which is a great service, btw. So cutting the size down on the backups sent to [Tarsnap][4] will save me a bit of money. <del>I&#8217;ll be doing an article later on that focuses entirely on Tarsnap.</del>. I&#8217;m pretty in love with it. You can find an article about [installing and using Tarsnap, right here at longren.io][5].  


<div class="wp-block-image">
  <figure class="aligncenter"><a href="https://i0.wp.com/longren.io/wp-content/uploads/2014/08/tarsnap.png"><img loading="lazy" width="429" height="96" src="https://i0.wp.com/longren.io/wp-content/uploads/2014/08/tarsnap.png?resize=429%2C96" alt="Online backups for the truly paranoid" class="wp-image-7306" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/08/tarsnap.png?w=429&ssl=1 429w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/08/tarsnap.png?resize=150%2C33&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/08/tarsnap.png?resize=300%2C67&ssl=1 300w" sizes="(max-width: 429px) 100vw, 429px" data-recalc-dims="1" /></a><figcaption>A secure online backup service.</figcaption></figure>
</div>

Anyway, here&#8217;s the command I use to backup and compress all databases on my MySQL server: 

<pre class="wp-block-preformatted">mysqldump -uroot -p --opt --all-databases | bzip2 -cq9 &gt; /home/tyler/mysql-backups/backupname.sql.bz2</pre>

That will create a backup of all databases. The `-cq9` piece in the `bzip2` command uses stdin for input and tells bzip2 to be quiet. The number, 9, specifies the compression level that bzip2 should use.

The script embedded in [the Gist below][6] is what I use to all my databases to _/home/tyler/mysql-backups/_, and then that folder gets backed up to [Tarsnap][4].  
https://gist.github.com/tlongren/85e0d7d04cd507b1ec53

To restore the database, you&#8217;ll want to `bunzip2` the `.sql.bz2` file first: 

<pre class="wp-block-preformatted">bunzip2 backupname.sql.bz2</pre>

That will leave you with a `backupname.sql` file. Then bring the resulting `.sql` file into MySQL like so: 

<pre class="wp-block-preformatted">mysql -uroot -pyourpasswordfornoprompt &lt; backupname.sql</pre>

The databases will need to either already exist, or there will need to be `CREATE DATABASE` statements in the `.sql` file. It&#8217;s up to you. I like to create my databases before hand, but it&#8217;s just personal preference.

That&#8217;s all there is to it. How do you take care of your backups? I&#8217;d love to hear how others are doing it. Comments are open.

There&#8217;s a [thread going on at Hacker News][7], too.

**Update:** Made a slight modification to the code and gist [suggested by sluggo][8].

**Update 2:** HackerNews user [Nanzikambe][9] suggested the [method above will destroy disk I/O on your server][10]. He [suggests using ZFS snapshots][11] instead. The example he posted is in the Gist below, and includes the ability to send the backup to a remote server. A good [tutorial on backing up MySQL using ZFS can be found here][12].  
  
<figure class="wp-block-embed is-type-rich is-provider-embed-handler">

<div class="wp-block-embed__wrapper">
  <div class="oembed-gist">
    <noscript>
      View the code on <a href="https://gist.github.com/tlongren/0e04f8efbc88ff793b51">Gist</a>.
    </noscript>
  </div>
</div></figure> 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7295"
					data-ulike-nonce="9dccce7ce0"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7295"></button><span class="count-box"></span>
  </div>
</div>

[][13]{.later-button-el}

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

 [1]: http://www.bzip.org/
 [2]: http://dev.mysql.com/doc/refman/5.1/en/mysqldump.html
 [3]: http://superuser.com/questions/205223/pros-and-cons-of-bzip-vs-gzip
 [4]: https://www.tarsnap.com
 [5]: https://longren.io/install-tarsnap-on-digitalocean-or-any-ubuntu-14-04-lts-system/
 [6]: https://gist.github.com/tlongren/85e0d7d04cd507b1ec53
 [7]: https://news.ycombinator.com/item?id=8131989
 [8]: http://longren.io/backup-and-compress-mysql-in-one-command/#comment-1526870151
 [9]: https://news.ycombinator.com/user?id=Nanzikambe
 [10]: https://news.ycombinator.com/item?id=8132187
 [11]: https://gist.github.com/tlongren/0e04f8efbc88ff793b51
 [12]: http://blog.danmassey.net/?p=962
 [13]: #