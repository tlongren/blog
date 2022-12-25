---
title: WordPress 2.0.4 Released
author: Tyler Longren
type: post
date: 2006-07-29T13:20:11+00:00
url: /wordpress-204-released/
views:
  - 13
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - blog
  - blogs
  - Open Source
  - opensource
  - Security
  - upgrade
  - WordPress
  - wordpress-2.0.4

---
[WordPress][1] [2.0.4 has been released][2].

> WordPress 2.0.4, the latest stable release in our Duke series, is available for immediate download. This release contains several important security fixes, so it’s highly recommended for all users. We’ve also rolled in a number of bug fixes (over 50!), so it’s a pretty solid release across the board.

I can&#8217;t find any documentation stating the user registration vulnerability has been fixed, but [Kelson is reporting][3] it has been taken care of in WordPress 2.0.4. I believe this WordPress release was pushed out quickly due to [some information][4] [revealed by Dr. Dave][5] earlier in the week.

I&#8217;m still not 100% sure that the problems pointed out by Dr. Dave have been fixed. Can anyone confirm that it has been? For those interested, [here&#8217;s a list of bugs that have been closed][6] as of the 2.0.4 release [[via Dougal Campbell][7]].

**UPDATE:** WordPress 2.0.4 does indeed fix the user registration vulnerability. [Dr. Dave has done some testing of his own][8] and seems pretty sure this vuln is fixed. It&#8217;s still probably a good idea to disable user registration just to be safe:

> As for the “users can register” option: enabling it back should be OK.  
> I personally will leave it off on my blogs, as I just don’t feel like entrusting strangers with access to wp-admin in the current state of the code (I insist that the aforementioned exploit has been fixed now, I am only being paranoid here).

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2187"
					data-ulike-nonce="77a6e0bd90"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2187"></button><span class="count-box"></span>
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

 [1]: http://www.wordpress.org/
 [2]: http://wordpress.org/development/2006/07/wordpress-204/
 [3]: http://www.hyperborea.org/journal/archives/2006/07/28/wp-204/
 [4]: http://unknowngenius.com/blog/archives/2006/07/26/critical-announcement-to-all-wordpress-users/
 [5]: http://unknowngenius.com/blog/archives/2006/07/27/followup-on-wordpress/
 [6]: http://trac.wordpress.org/query?status=closed&milestone=2.0.4
 [7]: http://dougal.gunters.org/blog/2006/07/28/wordpress-204
 [8]: http://unknowngenius.com/blog/archives/2006/07/27/followup-on-wordpress/#comment-78759
 [9]: #