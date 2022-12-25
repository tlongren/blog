---
title: Automate Taking Snapshots of Your DigitalOcean Droplets with DOSnapshot
author: Tyler Longren
type: post
date: 2014-09-16T12:56:40+00:00
url: /automate-making-snapshots-of-your-digitalocean-droplets/
featured_image: /wp-content/uploads/2014/09/dosnapshot1.png
independent_publisher_primary_category:
  - DigitalOcean
dsq_thread_id:
  - 3018352032
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cool
  - digitalocean
  - git
  - GitHub
  - hosting
  - Internet
  - Linux
  - Open Source
  - Personal
  - tools

---
 

## Multi-threading. Auto-cleanup. Cron optimized.

There are a lot of [neat tools][1] people have built for [DigitalOcean][2]. 

The app I&#8217;m really in love with is [DOSnapshot][3], and is [hosted on GitHub][4]. DOSnapshot does exactly what its name would suggest, it takes snapshots of your droplets.

As of this post, I&#8217;m the only one that&#8217;s [left a comment on the DOSnapshot Community Projects page][5], which took me a bit by surprise, given the quality of the tool.

Taking a snapshot of a [DigitalOcean][2] Droplet is essentially like making an exact copy of the Droplet (server) that you can then use again at a later time. Very useful for scaling and updating a Droplet to a newer version of your Linux distribution without losing all of the Droplet&#8217;s configuration.

[Etel Sverdlov][6] does a very good job of [explaining the difference between snapshots and backups in this DigitalOcean community tutorial][7]. I suggest you read it if you&#8217;re unsure what the differences between a backup and snapshot are.

### 1. Install DOSnapshot

[DOSnapshot][8] can be installed as a ruby gem, which is what I chose to do because it&#8217;s just so easy. **Don&#8217;t install this on your DigitalOcean Droplet!** It&#8217;s meant to run from your local machine. Installing DOSnapshot as a Rubygem is as simple as: 

<pre class="wp-block-preformatted">sudo gem install do_snapshot</pre>

Pre-built binaries are also provided for Linux users, and [OSX users have the option of installing via Homebrew Tap][9].

### 2. Set Your DigitalOcean Client ID and API Key

Once you&#8217;ve got it installed, you&#8217;ll need to set your DigitalOcean Client ID and API Key. You can set them as environment variables, or you can pass them as parameters when actually running DOSnapshot. This is straight from the README:

<blockquote class="wp-block-quote">
  <p>
    First you may need to set DigitalOcean API keys:
  </p>
  
  <p>
    $ export DIGITAL_OCEAN_CLIENT_ID=&#8221;SOMEID&#8221;<br /> $ export DIGITAL_OCEAN_API_KEY=&#8221;SOMEKEY&#8221;
  </p>
  
  <p>
    If you want to set keys without environment, than set it via options when you run do_snapshot:
  </p>
  
  <p>
    $ do_snapshot &#8211;digital-ocean-client-id YOURLONGAPICLIENTID &#8211;digital-ocean-api-key YOURLONGAPIKEY
  </p>
</blockquote>

### 3. Take A Snapshot

Please remember that running the `do_snapshot` command will cause your droplet to shutdown so the snapshot can be taken.

DOSnapshot has a pretty large number of options that you can specify. I&#8217;m going to keep this simple so you get the basics of it. Learning a few of the main options will be mostly what you need to know, after you&#8217;ve got them figured out, setting up a cronjob is cake.

You can take snapshots of all of your droplets at once, you can specify which droplets to take snapshots of, and you can specify droplets that you don&#8217;t want to take a snapshot of. I typically take a snapshot of a single droplet at a time, and I do it like this: 

<pre class="wp-block-preformatted">do_snapshot --only 1111 -k 3 -c -v</pre>

The above will take a snapshot of only one droplet, a droplet with an ID of _1111_, replace _1111_ with the ID of your droplet. You can find your droplets ID in your browser URL bar while managing the droplet. So if you see _https://cloud.digitalocean.com/droplets/1234567_, your droplet&#8217;s ID is _1234567_.

Here&#8217;s all of [the options][10].  
<figure class="wp-block-embed is-type-rich is-provider-embed-handler">

<div class="wp-block-embed__wrapper">
  <div class="oembed-gist">
    <noscript>
      View the code on <a href="https://gist.github.com/tlongren/efe006201b291acf89a7">Gist</a>.
    </noscript>
  </div>
</div></figure> 

### 4. Scheduling With Cron

First, you must have cron installed. There&#8217;s plenty of [tutorials][11] on how to do that. That tutorial even explains how to configure a cron job using the _crontab_ utility. There&#8217;s an example crontab entry in the [DOSnapshot README][12]. Mine is pretty simple: 

<pre class="wp-block-preformatted">0 4 * * 2 do_snapshot --only 1111 -k 3 -c -v</pre>

If you have questions about setting any of this up, feel free to leave a comment!

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7460"
					data-ulike-nonce="0ba546946a"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7460"></button><span class="count-box"></span>
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

 [1]: https://www.digitalocean.com/community/projects
 [2]: https://www.digitalocean.com/?refcode=cbf49d0481c8
 [3]: https://www.digitalocean.com/community/projects/dosnapshot
 [4]: https://github.com/merqlove/do_snapshot
 [5]: https://www.digitalocean.com/community/projects/dosnapshot?comment=18377
 [6]: https://www.digitalocean.com/community/users/etel
 [7]: https://www.digitalocean.com/community/tutorials/digitalocean-backups-and-snapshots-explained
 [8]: http://dosnapshot.merqlove.ru/
 [9]: https://github.com/merqlove/homebrew-do-snapshot
 [10]: https://gist.github.com/tlongren/efe006201b291acf89a7
 [11]: https://www.digitalocean.com/community/tutorials/how-to-use-cron-to-automate-tasks-on-a-vps
 [12]: https://github.com/merqlove/do_snapshot/blob/master/README.md
 [13]: #