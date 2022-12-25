---
title: Easily Deploy An Open Source Team Chat App to Heroku
author: Tyler Longren
type: post
date: 2014-04-10T08:05:06+00:00
url: /easily-deploy-an-open-source-team-chat-app-to-heroku/
featured_image: /wp-content/uploads/2014/04/lets-chat.jpg
dsq_thread_id:
  - 2590134907
full_width_featured_image:
  - 1
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - awesome
  - chat
  - GitHub
  - heroku
  - hosting
  - Internet
  - JavaScript
  - Open Source
  - opensource
  - Personal

---
 

## Self-hosted chat app for small teams {.subtitle}

[Let&#8217;s Chat][1] is a pretty cool piece of software (no, it&#8217;s actually fucking awesome). The ability to run the app on Heroku just makes it that much nicer.

Setting it up on Heroku is quite easy. You can see it running on Heroku at [http://yell.longren.io][2]. There&#8217;s no admin user, so anyone can register and create their own rooms.

Files can also be posted to rooms, but an Amazon S3 bucket is required for that feature to work. Although, other file storage options are being looked into. Another neat feature is automatic transcript creation. There&#8217;s a transcript screenshot in the gallery below.

### Prepare Let&#8217;s Chat

Open up a terminal and clone the Let&#8217;s Chat Git repository:

<pre class="EnlighterJSRAW" data-enlighter-language="shell" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">git clone https://github.com/sdelements/lets-chat.git</pre>

That will make a local clone of Let&#8217;s Chat in the `lets-chat` folder. Go into that folder, with <span class="lang:sh decode:true  crayon-inline ">cd lets-chat</span>.

**1.** Copy settings.js.sample to **settings.js**, like so:

<pre class="EnlighterJSRAW" data-enlighter-language="shell" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">cp settings.js.sample settings.js</pre>

**2.** Remove `settings.js` from the `.gitignore` file. Just open `.gitignore` in your favorite text editor and remove the line containing `settings.js`.

**3.** Make any changes to `settings.js` that you&#8217;d like. This is where you&#8217;d specify your Amazon S3 credentials to allow storing files in a bucket.

## Deploy To Heroku

We&#8217;ll be using `heroku-app-name` as the name of our Heroku app. So you&#8217;ll obviously need to change instances of `heroku-app-name` in the commands that follow.

**1.** Add a Heroku remote to your newly cloned repository:

<pre class="EnlighterJSRAW" data-enlighter-language="shell" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">heroku git:remote -a heroku-app-name</pre>

**2.** Add the MongoLab Heroku addon:

<pre class="EnlighterJSRAW" data-enlighter-language="shell" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">heroku addons:add mongolab -a heroku-app-name</pre>

**3.** Get the **Mongo URL**. Executing the following will give you the **Mongo URL**, which you&#8217;ll need below.

<pre class="EnlighterJSRAW" data-enlighter-language="shell" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">heroku config:set DATABASE_URL=`heroku config:get MONGOLAB_URI -a heroku-app-name` -a heroku-app-name</pre>

You&#8217;ll see some output similar to this:

<pre class="EnlighterJSRAW" data-enlighter-language="shell" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">Setting config vars and restarting heroku-app-name... done, v7
DATABASE_URL: mongodb://heroku_app11111111:111aaaa1aaaaa11a111a1aa1aa@aa111111.mongolab.com:39707/heroku_app11111</pre>

The **Mongo URL** is the part that starts with `mongodb://`.

**4.** Now, we need to set the Mongo URL:

<pre class="EnlighterJSRAW" data-enlighter-language="shell" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">heroku config:set DATABASE_URL=mongodb://heroku_app11111111:111aaaa1aaaaa11a111a1aa1aa@aa111111.mongolab.com:39707/heroku_app11111 -a heroku-app-name</pre>

You&#8217;ll want to change the **DATABASE_URL** variable to the **Mongo URL** specific to your app.

**6.** All that&#8217;s left is to commit and push to Heroku. You should still be in the **lets-chat** folder, so, make a git commit! You&#8217;ll have to anyway, before you can push to Heroku.

<pre class="EnlighterJSRAW" data-enlighter-language="shell" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">git commit -am "Initial commit."</pre>

**7.** Now we can finally push this to Heroku!

<pre class="EnlighterJSRAW" data-enlighter-language="shell" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">git push heroku master</pre>

Visit your Heroku app URL in your web browser and you should be greeted with a screen that looks similar to the featured image for this post. Some basic screenshots can be seen below!

<div class="wp-block-jetpack-tiled-gallery aligncenter is-style-rectangular">
  <div class="tiled-gallery__gallery">
    <div class="tiled-gallery__row">
      <div class="tiled-gallery__col">
        <figure class="tiled-gallery__item"><a href="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-1024x338.jpg?ssl=1"><img srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-1024x338.jpg?strip=info&#038;w=600&#038;ssl=1 600w,https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-1024x338.jpg?strip=info&#038;w=900&#038;ssl=1 900w,https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-1024x338.jpg?strip=info&#038;w=1200&#038;ssl=1 1200w,https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-1024x338.jpg?strip=info&#038;w=1500&#038;ssl=1 1500w,https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-1024x338.jpg?strip=info&#038;w=1721&#038;ssl=1 1721w" alt="" aria-label="image 1 of 3 in gallery" data-height="569" data-id="6399" data-link="https://www.longren.io/easily-deploy-an-open-source-team-chat-app-to-heroku/lets-chat/" data-url="https://www.longren.io/wp-content/uploads/2014/04/lets-chat-1024x338.jpg" data-width="1721" src="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-1024x338.jpg?ssl=1" /></a></figure>
      </div>
    </div>
    
    <div class="tiled-gallery__row">
      <div class="tiled-gallery__col">
        <figure class="tiled-gallery__item"><a href="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-room-list-1024x393.png?ssl=1"><img srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-room-list-1024x393.png?strip=info&#038;w=600&#038;ssl=1 600w,https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-room-list-1024x393.png?strip=info&#038;w=900&#038;ssl=1 900w,https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-room-list-1024x393.png?strip=info&#038;w=1068&#038;ssl=1 1068w" alt="" aria-label="image 2 of 3 in gallery" data-height="410" data-id="6306" data-link="https://www.longren.io/easily-deploy-an-open-source-team-chat-app-to-heroku/lets-chat-room-list/" data-url="https://www.longren.io/wp-content/uploads/2014/04/lets-chat-room-list-1024x393.png" data-width="1068" src="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-room-list-1024x393.png?ssl=1" /></a></figure>
      </div>
    </div>
    
    <div class="tiled-gallery__row">
      <div class="tiled-gallery__col">
        <figure class="tiled-gallery__item"><a href="https://i2.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-room-1024x608.png?ssl=1"><img srcset="https://i2.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-room-1024x608.png?strip=info&#038;w=600&#038;ssl=1 600w,https://i2.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-room-1024x608.png?strip=info&#038;w=900&#038;ssl=1 900w,https://i2.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-room-1024x608.png?strip=info&#038;w=1068&#038;ssl=1 1068w" alt="" aria-label="image 3 of 3 in gallery" data-height="635" data-id="6305" data-link="https://www.longren.io/easily-deploy-an-open-source-team-chat-app-to-heroku/lets-chat-room/" data-url="https://www.longren.io/wp-content/uploads/2014/04/lets-chat-room-1024x608.png" data-width="1068" src="https://i2.wp.com/www.longren.io/wp-content/uploads/2014/04/lets-chat-room-1024x608.png?ssl=1" /></a></figure>
      </div>
    </div>
  </div>
</div>

If you run into any issues or find something I have incorrect, please let me know. You could also see if your problem has [already been addressed on GitHub][3].

This is the steps I took to get Let&#8217;s Chat working on Heroku. It&#8217;s possible that the project developers will streamline this process in the future. But for now, this is a very easy solution to hosting on Heroku.

Let&#8217;s Chat is brought to you by [SD Elements][4], an application security company out of Canada. [Check them out][4].

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="6288"
					data-ulike-nonce="f679bc46d9"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_6288"></button><span class="count-box"></span>
  </div>
</div>

[][5]{.later-button-el}

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

 [1]: https://github.com/sdelements/lets-chat
 [2]: http://yell.longren.io/
 [3]: https://github.com/sdelements/lets-chat/issues
 [4]: http://sdelements.com/
 [5]: #