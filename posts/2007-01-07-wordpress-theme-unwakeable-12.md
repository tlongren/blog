---
title: 'WordPress Theme: Unwakeable 1.2'
author: Tyler Longren
type: post
date: 2007-01-07T07:40:26+00:00
url: /wordpress-theme-unwakeable-12/
views:
  - 43170
ratings_users:
  - 45
ratings_score:
  - 189
ratings_average:
  - 4.2
DiggUrl:
  - http://www.longren.org/2007/01/07/wordpress-theme-unwakeable-12/
dsq_thread_id:
  - 1385925448
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - blog
  - blogging
  - design
  - Internet
  - Noteworthy
  - Personal
  - PHP
  - style
  - themes
  - Unwakeable
  - WordPress
  - wordpress-theme

---
[Unwakeable 1.2][1] is out! You can [download it][2] or you can [visit the Unwakeable page][1] for some more details. You may also be interested in the [ChangeLog][3], although I&#8217;ll go over a number of the changes in this post.

Probably the most notable change is the separate options for Unwakeable in the wp_options table. Let me explain a little bit. Basically, I&#8217;ve renamed the options to be unwakeable specific. Previously, Unwakeable would pick up options already set in K2 or it would just set the default values, still with the K2 names. So, if you&#8217;re upgrading to Unwakeable 1.2 from an earlier version, you&#8217;ll want to click the &#8220;Copy Options&#8221; button from the Unwakeable Options page. Clicking that button will take the options you had set in previous versions and will update them to work with Unwakeable 1.2. You can also copy your options from K2 to Unwakeable 1.2 with this button. If you&#8217;re installing Unwakeable for the first time, this probably doesn&#8217;t apply to you.

Now, if you&#8217;d rather not copy your old options over, that&#8217;s OK. You can just go into the Unwakeable Options page and set the options as you normally would. If this scares you, don&#8217;t worry, you can&#8217;t really break anything by not copying options over. Really, you can&#8217;t break anything even if you do want to copy your previous options over. If you have any questions, just [get in touch with me][4].

I&#8217;ve also added support for two more plugins, [Landing Sites][5] and [Gregarious][6]. Gregarious is a replacement for the Digg This Reloaded plugin, which is now dead. Unwakeable 1.2 still has support for the [Digg Integrator plugin][7] also. I suggeset you use Gregarious if you want Digg buttons on your pages. It makes use of the new Digg API where Digg Integrator loads Digg buttons in an iframe, not the ideal way to display Digg buttons these days.

Now, you may be wondering why I built in support for Gregarious. Gregarious has a feature called auto-append that will automatically place a Digg button on your page. However, that feature isn&#8217;t enabled by default. And, there&#8217;s no option to place the Digg button in the sidebar with the auto-append feature. So, I added some code that will detect if auto-append is enabled. If auto-append is enabled, the Digg button isn&#8217;t displayed on the sidebar. However, if auto-append isn&#8217;t enabled, the Digg button will be displayed in the sidebar. That way you still have the option of displaying the Digg button in your sidebar, even if you use Gregarious.

Also, I&#8217;ve made a small fix to the CSS that should get rid of the few pixels of whitespace that were showing in the header, between the black and gray sections. The black in the header is now flush with the right side of the page. You can see what it looked like previously [in this image][8]. And you can see it fixed [in this image][9] (or right here on this blog). I&#8217;d like to thank [Jason][10] for pointing out that whitespace.

Is there anything you guys would like to see in the next version of Unwakeable? Could be anything from support for a plugin to design changes. Anything? Anybody?

Enjoy this new version and let me know if you have any problems getting Unwakeable functioning properly. I will provide almost unlimited support for people having issues with Unwakeable. Although, I won&#8217;t always be able to support Unwakeable if you&#8217;ve made numerous changes to the CSS or PHP for your site.

And lastly, a big &#8220;thank you&#8221; to everyone who is using Unwakeable. I never anticipated that this theme would become so popular. At my last rough count, there&#8217;s about 300 blogs using Unwakeable, I expected maybe 20. 🙂 Thanks again everyone for your support! It&#8217;s now far past my bed time&#8230; 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2293"
					data-ulike-nonce="40ec162fe2"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2293"></button><span class="count-box"></span>
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

 [1]: http://www.longren.org/unwakeable/
 [2]: http://longren.org/files/unwakeable-1.2.zip
 [3]: http://www.longren.org/unwakeable/#changelog
 [4]: http://www.longren.org/contact/
 [5]: http://theundersigned.net/2006/06/landing-sites-11
 [6]: http://dev.lipidity.com/feature/wp-plugin-gregarious
 [7]: http://bill2me.com/digg-integrator/
 [8]: http://www.flickr.com/photos/tlongren/348651760/
 [9]: http://www.flickr.com/photos/tlongren/348651761/
 [10]: http://www.threesixty101.com/
 [11]: #