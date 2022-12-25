---
title: 'Placezombie: The Zombie Image Placeholder Service'
author: Tyler Longren
type: post
date: 2014-10-23T12:49:11+00:00
url: /introducing-placezombie-the-zombie-image-placeholder-service/
featured_image: /wp-content/uploads/2014/10/placezombie.png
independent_publisher_primary_category:
  - Services
dsq_thread_id:
  - 3146518058
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cool
  - Funny
  - git
  - GitHub
  - hosting
  - Internet
  - Open Source
  - services

---
## Zombie Image Placeholders Are Back {.subtitle}

And just in time for Halloween!

I wrote a post about my [10 favorite image placeholder services][1] a while ago. Placezombies.com was one of them. Here&#8217;s the [announcement blog post][2] for Placezombies.com.

Down in the comments, you&#8217;ll see that the owners forgot to renew the domain name, so it obviously stopped working. The source was [posted on GitHub][3], so I immediately [forked it][4] and got to work setting up a replacement.

A quick check revealed that [placezombie.com][5] was available, so I registered it. Score.

I really didn&#8217;t want to host this at [DigitalOcean][6] like I typically would, not knowing what to expect for bandwidth usage. Instead, I chose to host it at [Heroku][7], using their free service.

Had a few issues getting it running, but after removing some Ruby stuff and creating the Procfile and package.json files that Heroku requires, I was almost good to go. Only thing holding me back was to [replace the port number node.js was using with the port that Heroku uses][8]. Did another `git push heroku master`, navigated to <http://placezombie.com> and there it was!

Here&#8217;s a 700&#215;300 zombie below for proof!

![Placezombie.com][9] 

That was generated like so:

<pre class="lang:xhtml decode:true " >&lt;img src="http://placezombie.com/700x300" alt="Placezombie.com" /&gt;</pre>

You can do black and white images, too:  
![Placezombie.com][10] 

That was generated like so:

<pre class="lang:xhtml decode:true " >&lt;img src="http://placezombie.com/g/700x300" alt="Placezombie.com" /&gt;</pre>

So, [add some gore to your mock-ups][11], just make sure your clients aren&#8217;t too squeamish.  
<img src="//placezombie.com/600x100" alt="Placezombie.com" class="aligncenter" /> 

My 5 year old daughter is obsessed with Zombies and is going to fucking love this. She wants to be a Zombie Elsa (from the movie Frozen) for Halloween. `:)` 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7588"
					data-ulike-nonce="b033e279f8"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7588"></button><span class="count-box"></span>
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

 [1]: https://longren.io/image-placeholders/
 [2]: http://www.metaltoad.com/blog/placezombies
 [3]: https://github.com/metaltoad/memeplacer
 [4]: https://github.com/tlongren/memeplacer
 [5]: http://placezombie.com/
 [6]: https://www.digitalocean.com/?refcode=cbf49d0481c8
 [7]: http://heroku.com
 [8]: https://github.com/tlongren/memeplacer/commit/729aee613f5addc66c448f295bd6426df68965ac
 [9]: //placezombie.com/700x300
 [10]: //placezombie.com/g/700x300
 [11]: http://placezombie.com
 [12]: #