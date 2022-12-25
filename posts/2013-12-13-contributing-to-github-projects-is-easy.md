---
title: Contributing To GitHub Projects is Easy
author: Tyler Longren
type: post
date: 2013-12-13T06:19:15+00:00
url: /contributing-to-github-projects-is-easy/
featured_image: /wp-content/uploads/2013/12/octocat.png
dsq_thread_id:
  - 2047393718
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
independent_publisher_primary_category:
  - GitHub
tags:
  - GitHub
  - how-to
  - howto
  - Internet
  - Open Source
  - Personal

---
Contributing code, or even just text, like documentation, to a [GitHub][1] repository that isn&#8217;t yours is extremely easy. I&#8217;ve seen a lot of people including instructions in their GitHub readme files explaining how to contribute to the project. I included instructions in the [Rootdip][2] readme at the [end of May 2013][3].

There&#8217;s so many repositories at GitHub, most of them contain some type of code. Some trending languages on GitHub are Javascript, C, CSS, PHP, Python, Ruby, and Shell. There&#8217;s still a lot of repositories that contain nothing but text, just like the [Front-end Frameworks repository][4].

<div class="wp-block-image">
  <figure class="alignleft"><a href="https://i2.wp.com/longren.io/wp-content/uploads/2013/12/github_trending.png"><img loading="lazy" width="1015" height="662" src="https://i2.wp.com/longren.io/wp-content/uploads/2013/12/github_trending.png?resize=1015%2C662" alt="GitHub Trending Repositories" class="wp-image-4897" srcset="https://i1.wp.com/www.longren.io/wp-content/uploads/2013/12/github_trending.png?w=1015&ssl=1 1015w, https://i1.wp.com/www.longren.io/wp-content/uploads/2013/12/github_trending.png?resize=300%2C195&ssl=1 300w" sizes="(max-width: 1015px) 100vw, 1015px" data-recalc-dims="1" /></a></figure>
</div>

GitHub provides [a list of trending repositories][5] as well. There&#8217;s some really, really good stuff there, there&#8217;s been times that I&#8217;ve starred every trending repository for the current day. I only have **608 stars**. You can see the trending repositories on the right side of [the Trending repositories page][5].

# So how the hell do I contribute?

First, find the repository you want to contribute to. Sounds obvious, but don&#8217;t contribute to a project that hasn&#8217;t been updated in 4 years, your contribution will never be integrated. For this example we&#8217;ll be adding a new navigation menu (it&#8217;s a website, but can be anything really) to the githubuser/the-project-name repository (it&#8217;s not real).

# Here&#8217;s what you want to do

### **1.** Fork the project

### **2.** Clone your forked repo: <span class="lang:default decode:true  crayon-inline ">git clone git@github.com:githubuser/the-project-name.git</span>

### **3.** Create your feature branch: <span class="lang:default decode:true  crayon-inline ">git checkout -b new-menu</span>

### **4.** Make your changes, creating whatever new files you need as well

### **5.** Commit your changes to your new branch: <span class="lang:default decode:true  crayon-inline ">git commit -am &#8216;Add a new menu to replace that ugly one&#8217;</span>

### **6.** Push to the branch: <span class="lang:default decode:true  crayon-inline ">git push origin new-menu</span>

### **7.** Create a new Pull Request!

To create a Pull Request, go to the original repo (ex: http://github.com/githubuser/the-project-name/). There should be a green &#8220;Compare and pull request&#8221; button (button image is below) that&#8217;s not typically there, _**click it**_! Enter your comments and wait for the repo owner to merge your branch or suggest some changes.

Remember, your pull request may never get merged, so make sure you contribute to an active project. I recently sent [a pull request to wp-svbtle][6], but the project hasn&#8217;t been active for 3 months. I&#8217;m also not sure the repo owner will accept my change, because my addition certainly isn&#8217;t inline with the official [svbtle.com][7].<figure class="wp-block-image">

[<img loading="lazy" width="196" height="29" src="https://i2.wp.com/longren.io/wp-content/uploads/2013/12/pull-request-button.png?resize=196%2C29" alt="GitHub Pull Request Button" class="wp-image-4893" data-recalc-dims="1" />][8]</figure> 

Here&#8217;s the &#8220;Compare and pull request&#8221; button for easy reference:  


Click that button and you&#8217;ll be taken to a form to enter a comment including details about your pull request. Fill out, submit the form, and you&#8217;re done. Congratulations! You just sent a pull request on GitHub! You&#8217;re almost guaranteed to find a project that you&#8217;d like to contribute to, so make use of the [issue search functionality][9], or the [advanced search][10] if you&#8217;re so inclined. There&#8217;s currently 21.7 million issues and 9.8 million repositories!

For the curious here&#8217;s a few recent pull requests I&#8217;ve sent that are strictly text-based, no code involved. I think they&#8217;re quite easy for git beginners to get a decent grasp of how git works. And getting people involved in open source at some level is always good.

Pull request examples:  
1. [StackLayout][11]  
2. [bootmetro][12]  
3. [IVORY Framework][13]

Did I mess something up? Tell me in the comments below, or [on Hacker News][14]. If there&#8217;s a better way that I should be doing this, I&#8217;d love to hear your suggestions. `:)`

[Enjoy a nyanoctocat][15].

<div class="wp-block-image">
  <figure class="aligncenter"><a href="https://i1.wp.com/longren.io/wp-content/uploads/2013/12/nyantocat.gif"><img loading="lazy" width="500" height="500" src="https://i1.wp.com/longren.io/wp-content/uploads/2013/12/nyantocat.gif?resize=500%2C500" alt="nyantocat" class="wp-image-4923" data-recalc-dims="1" /></a></figure>
</div>

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="4884"
					data-ulike-nonce="8e29287a0a"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_4884"></button><span class="count-box"></span>
  </div>
</div>

[][16]{.later-button-el}

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

 [1]: http://github.com
 [2]: https://longren.io/wordpress/rootdip/
 [3]: https://github.com/tlongren/rootdip/commit/338275b0bc05bd0aa1b6b2c4477f03174098f425
 [4]: https://github.com/usablica/front-end-frameworks
 [5]: https://github.com/trending
 [6]: https://longren.io/add-post-thumbnails-to-wp-svbtle/
 [7]: http://svbtle.com/
 [8]: http://github.com/tlongren/
 [9]: https://github.com/search
 [10]: https://github.com/search/advanced
 [11]: https://github.com/usablica/front-end-frameworks/pull/88
 [12]: https://github.com/usablica/front-end-frameworks/pull/86
 [13]: https://github.com/usablica/front-end-frameworks/pull/89
 [14]: https://news.ycombinator.com/item?id=6899346
 [15]: http://octodex.github.com/nyantocat/
 [16]: #