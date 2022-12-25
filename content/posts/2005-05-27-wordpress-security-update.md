---
title: WordPress Security Update
author: Tyler Longren
type: post
date: 2005-05-27T17:38:44+00:00
url: /wordpress-security-update/
views:
  - 2018
dsq_thread_id:
  - 2214146854

---
Looks like there&#8217;s a security vulnerability in WordPress if you&#8217;re running the default theme. Here&#8217;s a little bit from the [WordPress Development Blog][1]:

> It has come to our attention that under certain circumstances there is a security vulnerability in WordPress that may be triggered if you’re running the default template. We were able to respond very quickly (under 40 minutes) and update the download to 1.5.1.2. You can upgrade by overwriting your old 1.5 files or if you would like to apply the fix manually it is relatively simple:
> 
> 1. Open the wp-includes/template-functions-category.php file in a text editor like Wordpad.  
> 2. Go to around line 103 where it says get\_the\_category\_by\_ID.  
> 3. Create a new line after that and paste in $cat\_ID = (int) $cat\_ID; 

Read about the [entire thing here][1]. Glad I&#8217;m not using the default theme! I&#8217;ve hacked this theme so much I wouldn&#8217;t be suprised if I&#8217;ve opened up some vulnerability&#8230;yah right. 😉 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="1902"
					data-ulike-nonce="d2dc39818b"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_1902"></button><span class="count-box"></span>
  </div>
</div>

[][2]{.later-button-el}

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

 [1]: http://wordpress.org/development/2005/05/security-update/
 [2]: #