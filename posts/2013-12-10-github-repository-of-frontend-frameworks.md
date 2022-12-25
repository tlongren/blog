---
title: GitHub Repository of Front-end Frameworks
author: Tyler Longren
type: post
date: 2013-12-11T05:56:39+00:00
url: /github-repository-of-frontend-frameworks/
featured_image: /wp-content/uploads/2013/12/Pure-e1386740444200.png
dsq_thread_id:
  - 2042858681
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - css
  - design
  - git
  - GitHub
  - Internet
  - kegplan.io
  - Personal
  - tools
  - ui

---
 

I&#8217;m partial to [Bootstrap][1], but have recently strayed away from it because I found myself relying too heavily on the default styles. Next I tried [Zurb Foundation][2] which I really liked. I used it to build the [VPSstat.us blog][3] and [main site][4].

There&#8217;s a crap ton of front-end frameworks. Some are barebones, like [Skeleton][5], and others are full featured, like [Bootstrap][1] and [Foundation][2].

To help make sense of it all, [usabli.ca][6] put together [a GitHub repository][7] dedicated to indexing all (or most) of the frontend frameworks. It&#8217;s definitely worth checking out, especially if you&#8217;re in the market for a new framework or just want to see what options are out there.

Lately I&#8217;ve been using [Purecss][8]. I think it&#8217;s a nice middle ground, providing just enough to get me going quickly on most projects. Purecss can also make use of some Bootstrap elements and scripts, [like modals][9]. I&#8217;ve been using Purecss with [kegplan.io][10]. It forces me to come up with design elements not part of the framework itself, but only where needed.

<div id="polls-10" class="wp-polls">
</div>

<div id="polls-10-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

**Update Dec 12, 2013:** A few comments were left noting some frameworks that are missing. I [added Layers CSS][11] and also [fixed the link to Twitter Bootstrap][12]. I&#8217;ve also created a branch to add the [Inuit.css framework][13], but there&#8217;s currently [a pull request pending to add Inuit CSS][14], however it seems to have stalled. So we&#8217;ll see if I can send a pull request in the next day or so for Inuit CSS.

I&#8217;ve also submitted pull requests for [StackLayout][15], [bootmetro][16], and hopefully Inuit CSS. I have a personal interest in this repository, so I&#8217;ll likely keep contributing to it.

Thanks to [Razvan for the Inuit suggestion][17], and [Naeem for the Layers suggestion][18]!

If there&#8217;s any other frameworks missing, which I&#8217;m sure there are, please mention them here and I&#8217;ll get them added to the repository. Or, you can even add to the repository yourself by sending a pull request. Here&#8217;s how I typically create a branch for a pull request.

  1. Clone the repo (_git clone git@github.com:usablica/front-end-frameworks.git_)
  2. Create your feature branch (_git checkout -b add-specific-framework_)
  3. Make your additions to README.md
  4. Commit your additions to your new branch (_git commit -am &#8216;Add some framework&#8217;_)
  5. Push to the branch (_git push origin add-specific-framework_)
  6. Create new Pull Request by going to the original repo. There should be a green &#8220;Compare and pull request&#8221; button that&#8217;s not typically there, _**click it**_! Enter your comments and wait for the repo owner to merge your branch or suggest some changes.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="4864"
					data-ulike-nonce="9c1f5d6472"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_4864"></button><span class="count-box"></span>
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

 [1]: http://getbootstrap.com/
 [2]: http://foundation.zurb.com/
 [3]: http://blog.vpsstat.us/posts/a-new-blog-design
 [4]: http://blog.vpsstat.us/posts/main-site-redesign-with-zurb-foundation
 [5]: http://www.getskeleton.com/
 [6]: https://github.com/usablica
 [7]: https://github.com/usablica/front-end-frameworks
 [8]: http://purecss.io/
 [9]: http://purecss.io/extend/#pure-bootstrap-javascript
 [10]: http://kegplan.io/
 [11]: https://github.com/usablica/front-end-frameworks/pull/84
 [12]: https://github.com/usablica/front-end-frameworks/pull/82
 [13]: http://inuitcss.com/
 [14]: https://github.com/usablica/front-end-frameworks/pull/38
 [15]: https://github.com/usablica/front-end-frameworks/pull/88
 [16]: https://github.com/usablica/front-end-frameworks/pull/86
 [17]: http://www.longren.org/github-repository-of-frontend-frameworks/#comment-1159759673
 [18]: http://www.longren.org/github-repository-of-frontend-frameworks/#comment-1158457171
 [19]: #