---
title: Introducing Passwds.io
author: Tyler Longren
type: post
date: 2014-11-02T14:03:44+00:00
url: /introducing-passwds-io/
featured_image: /wp-content/uploads/2014/11/passwdsio.png
independent_publisher_primary_category:
  - Services
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
dsq_thread_id:
  - 3182163708
tags:
  - cool
  - freelance
  - git
  - GitHub
  - Internet
  - JavaScript
  - Open Source
  - Personal
  - PHP
  - Security
  - services
  - tools

---
## Pronounceable Password Generator {.subtitle}

I&#8217;d had this code sitting around for a while and decided to [make a new site dedicated to it][1]. It&#8217;s called [passwds.io][1]. It&#8217;s a simple service that produces pseudo-random passwords that have some elements that can actually be pronounced, hopefully making them easier to remember.

I do not recall where I got the original code to generate the _pronounceable_ passwords, but am trying to find the source so I can credit where it&#8217;s deserved.

I threw thew site at [passwds.io][1] together in about an hour using the newest [Bootstrap][2], [PHP][3], and [jQuery][4].

[Brandon Lighter][5] brought up the fact that I could be [storing all generated passwords][6], but I&#8217;m not. This was developed as a tool for myself to use while I was a sys admin at a large local business, I&#8217;d use it to create new passwords for users in Active Directory. It&#8217;s still the same code.

Once I can bring the code to a level that isn&#8217;t so scattered, I will put it on GitHub so everyone can see the source and what&#8217;s going on. It&#8217;s really very, very simple.

Of course, I could omit the important &#8220;logging&#8221; piece when pushing to GitHub, but at some point people just have to trust others, and I&#8217;m flat out saying there&#8217;s no type of logging being done at [passwds.io][1], other than the standard [Google Analytics][7] and [Gaug.es][8] for site analytics/

Brandon does bring up good points though, like no usage of special characters.

> Secondly, they are only lower-case, upper-case, and numbers, which means you are pulling from a much smaller character set than you could be, making brute-force attacks easier. 

I may add an option to do pronounceable passwords, or passwords with special characters enabled, which would probably break pronounceability. But options are always nice.

If you have other suggestions, I&#8217;d love to hear them. I&#8217;ve debated adding user accounts and the ability to save your generated passwords (that would be accessible only by you), but that sort of goes beyond the scope of [passwds.io][1], which is simple, fast password password creation.

An example output from passwds.io can be seen in the screenshot below.  
[<img loading="lazy" src="https://i1.wp.com/longren.io/wp-content/uploads/2014/11/passwdsio-results-1024x538.png?resize=700%2C367" alt="passwdsio-results" width="700" height="367" class="aligncenter size-large wp-image-7653" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/11/passwdsio-results.png?resize=1024%2C538&ssl=1 1024w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/11/passwdsio-results.png?resize=150%2C78&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/11/passwdsio-results.png?resize=300%2C157&ssl=1 300w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/11/passwdsio-results.png?resize=700%2C367&ssl=1 700w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/11/passwdsio-results.png?w=1239&ssl=1 1239w" sizes="(max-width: 700px) 100vw, 700px" data-recalc-dims="1" />][9]

Also, check out [Placezombie.com][10] if you&#8217;re looking for some pretty gruesome zombie images to use as placeholder images in your designs. Sample 900&#215;150 pixel greyscale image below, achieved with <span class="lang:xhtml decode:true  crayon-inline " >https://placezombie.com/g/900&#215;150</span> :  
![][11] 

Anyway, like I said, I&#8217;d love to hear your thoughts on [passwds.io][12]. Leave a comment here, it&#8217;s the best way to communicate with me about [passwds.io][12]. I haven&#8217;t bothered setting up passwds.io email yet. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7645"
					data-ulike-nonce="0ac05729af"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7645"></button><span class="count-box"></span>
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

 [1]: https://passwds.io
 [2]: http://getbootstrap.com/
 [3]: http://php.net
 [4]: http://jquery.com/
 [5]: http://therosettadrake.blogspot.com
 [6]: http://therosettadrake.blogspot.com/2014/11/justification-for-your-paranoia.html
 [7]: https://www.google.com/analytics/
 [8]: http://get.gaug.es/
 [9]: https://i1.wp.com/longren.io/wp-content/uploads/2014/11/passwdsio-results.png?ssl=1
 [10]: https://placezombie.com/
 [11]: https://placezombie.com/g/900x150
 [12]: https://passwds.io/
 [13]: #