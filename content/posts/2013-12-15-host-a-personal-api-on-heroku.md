---
title: Host a Personal Data API on Heroku
author: Tyler Longren
type: post
date: 2013-12-16T04:53:37+00:00
url: /host-a-personal-api-on-heroku/
featured_image: /wp-content/uploads/2013/12/beckman.png
dsq_thread_id:
  - 2053183985
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - api
  - cool
  - git
  - GitHub
  - heroku
  - Internet
  - json
  - node
  - Open Source
  - paas
  - Personal
  - PHP
  - stats

---
 

[Josh Beckman][1] makes some pretty cool stuff. One of my favorite creations of his is [Stark Lines][2]. He&#8217;s also got a pretty neat API on his site that allows others to query it to get information about him. It&#8217;s at <http://www.bckmn.com/api>. Some of Josh&#8217;s JSON is generated on the fly with data from other API&#8217;s, and is built with [Node.js][3].  
<figure class="wp-block-embed-twitter wp-block-embed is-type-rich is-provider-twitter">

<div class="wp-block-embed__wrapper">
  <blockquote class="twitter-tweet" data-width="550" data-dnt="true">
    <p lang="en" dir="ltr">
      <a href="https://twitter.com/tlongren?ref_src=twsrc%5Etfw">@tlongren</a> Some of it is calculated on the fly, some is pulled in from other APIs, and some is stored locally. Email me if you want more info
    </p>&mdash; Josh Beckman (@josh_beckman) 
    
    <a href="https://twitter.com/josh_beckman/status/410859346709344256?ref_src=twsrc%5Etfw">December 11, 2013</a>
  </blockquote>
</div></figure> 

You can make a similar API for your website really easily with a little PHP and [Heroku][4]. I [put the whole thing up on GitHub][5] so you can contribute (programming language examples especially) or totally make it your own.

I wanted to make it really easy for anyone to setup. You could get it setup with nothing but a text editor. Hosting your Personal API on heroku is quite nice as it provides great speeds and relatively good uptimes. Plus, if you&#8217;re a git fan, git push heroku master feels really good, lol.

<div id="polls-12" class="wp-polls">
</div>

<div id="polls-12-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

**Of course, there&#8217;s always some concerns.**

### 1. A Standard

Ideally, every &#8220;personal site&#8221; with an /api URL or api.* subdomain should contain the same info, or MOST of the info, probably just the basics like name, age, langues, and location (maybe). _If_ their was a standard it&#8217;d be very easy to grab info about LOTS of people, which may or may not be such a good idea. And that leads nicely to my next point

### 2. Privacy

There&#8217;s obviously some things you don&#8217;t want public, like your address and probably phone number. If you do implement a personal API like this, I suggest you modify the array to suit your needs. It&#8217;s extremely easy to edit, all it requires is a text editor, like Sublime Text. If there was a &#8220;Standard&#8221; personal API like mentioned above, it&#8217;s be very easy for attackers to just hit every website at /api or /api.php and pull down all the data.

## Enough with concerns, gimme more

The benefits are pretty endless, especially depending on what kind of info your API provides. For example, people can fetch my name, employer, age, blogs, sites I run, generic family information and various other things. Authentication would be a good idea, too. You could provide relatively harmless info, like name and age, to the general public, but could require an API key to get even more JSON. That way, you could give friends and family access to more information.

## Run It!

This is built to run on Heroku. Here&#8217;s a pretty basic way of deploying to Heroku.

  1. Fork [tlongren/personal-api][5] on GitHub and make a local clone.
  2. Install the [Heroku Toolbelt][6] and login to Heroku with the command &#8220;_**heroku login**_&#8220;. Enter your username and password to login with the Heroku Toolbelt.
  3. Create a new app on Heroku either through the web interface, or with the command &#8220;_**heroku create**_&#8220;. If you do it with the command line the app name will be shown to you, [see here][7].
  4. Open a terminal and go into the folder that you cloned your fork into and run the command &#8220;_**heroku git:remote -a heroku-app-name**_&#8220;. That will add a remote named &#8220;heroku&#8221; to your local clone.
  5. Now, while still in your local clone folder, run &#8220;_**git push heroku master**_&#8221; to push your app to Heroku. If your app is named &#8220;heroku-app-name&#8221;, you can access your app at http://heroku-app-name.herokuapp.com.

And that&#8217;s all there is to getting setup with Heroku, a total of 5 steps, with just 4 simple commands.

#### [See the GitHub repository for more info.][5]

See any issues or have any concerns? Leave a comment below or [at Hacker News][8].

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="4871"
					data-ulike-nonce="47f55875eb"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_4871"></button><span class="count-box"></span>
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

 [1]: http://www.bckmn.com/
 [2]: http://www.bckmn.com/stark-lines/
 [3]: http://nodejs.org/
 [4]: http://www.heroku.com/
 [5]: https://github.com/tlongren/personal-api
 [6]: https://toolbelt.heroku.com/
 [7]: https://devcenter.heroku.com/articles/git
 [8]: https://news.ycombinator.com/item?id=6912980
 [9]: #