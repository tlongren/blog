---
title: 'Blogpulse: Crawling Again'
author: Tyler Longren
type: post
date: 2005-10-14T16:16:26+00:00
url: /blogpulse-crawling-again/
views:
  - 1934
dsq_thread_id:
  - 1385908679
tags:
  - ajax
  - blog
  - blogpulse
  - blogs
  - broken
  - PHP
  - plugin
  - web-2.0
  - web2
  - web2.0
  - WordPress

---
I noticed last month that my [Blogpulse Profile page][1] was no longer staying up to date. According to them, my last post was on August 25th. I sent an e-mail asking if something was up on their end or if there was some problem on my end.

I finally got an e-mail back yesterday. It seems some code on this site was preventing their crawler from indexing anything. I&#8217;m not gonna post the code, who knows what it&#8217;ll do if I try posting it. The code basically looked like an HTML comment and contained the text &#8220;CDATA&#8221;.

Sure enough, the offending code in the e-mail was easily found when viewing the source at this site. I was sure something was wrong on the Blogpulse side of things, I couldn&#8217;t think of any changes I had made that would affect their ability to index this site. I was wrong.

I had switched the contact form over from [WP-ContactForm][2] to [Intouch][3]. I wanted to give Intouch a shot because it made use of AJAX mostly. It worked well so I stuck with it. Turns out Intouch was the source of the bad code that prevented the blogpulse crawlers from indexing me.

After reverting back to using the WP-ContactForm plugin, everything looks good. The offending code can no longer be found here. Still waiting for my Blogpulse Profile page to update though. I&#8217;d expect it to be back in sync by the end of the weekend.

I wonder what other blog services have been unable to crawl this site due to that code.

Linked @ [California Conservative][4], [Cao&#8217;s Blog][5], [The Political Teen][6], [Outside The Beltway][7], [Mudville Gazette][8], [Jo&#8217;s Cafe][9] and [MacStansbury][10]. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2043"
					data-ulike-nonce="fe4defa723"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2043"></button><span class="count-box"></span>
  </div>
</div>

[][11]{.later-button-el}

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

 [1]: http://www.blogpulse.com/profile?type=overview&url=http://www.longren.org
 [2]: http://ryanduff.net/projects/wp-contactform/
 [3]: http://adahas.com/work/intouch/
 [4]: http://www.californiaconservative.org/?p=1172
 [5]: http://caosblog.com/2299
 [6]: http://thepoliticalteen.net/2005/10/14/optrfri/
 [7]: http://www.outsidethebeltway.com/archives/12298
 [8]: http://www.mudvillegazette.com/archives/003699.html
 [9]: http://joscafe.com/2005/10/14/tgif-specials-16/
 [10]: http://macstansbury.org/open-threadopen-trackbacks-3
 [11]: #