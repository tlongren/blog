---
title: Use Google Hosted jQuery in WordPress
author: Tyler Longren
type: post
date: 2010-11-21T05:15:50+00:00
url: /use-google-hosted-jquery-in-wordpress/
ratings_users:
  - 2
ratings_score:
  - 10
ratings_average:
  - 5
views:
  - 156
dsq_thread_id:
  - 1577673292
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - code
  - google
  - Internet
  - jquery
  - Noteworthy
  - Personal
  - WordPress

---
So, I recently needed to use a [google hosted version of jquery][1] for a WordPress theme (don&#8217;t ask). I came across [this topic][2] at the WordPress forums.

User [bazil749][3] [suggested][4] doing this, I&#8217;ve updated it to include [jQuery 1.4.4][5]:

<pre>&lt;?php
if( !is_admin()){
	wp_deregister_script(&#39;jquery&#39;);
	wp_register_script(&#39;jquery&#39;, ("http://ajax.googleapis.com/ajax/libs/jquery/1.4.4/jquery.min.js"), false, &#39;1.4.4&#39;);
	wp_enqueue_script(&#39;jquery&#39;);
}
?&gt;
</pre>

I added that piece of code to the proper place in the header.php file for the theme and it worked like a champ. jQuery was now loading from Google. The [Use Google Libraries plugin][6] does the same basic thing, except it can use libraries other than just jQuery, like [jQuery UI][7], [Dojo][8], [MooTools][9], and [Protoype][10].

There are [a number of good reasons][11] to let Google host jQuery for you. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2617"
					data-ulike-nonce="519bcd1ad4"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2617"></button><span class="count-box"></span>
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

 [1]: http://code.google.com/apis/libraries/devguide.html#jquery
 [2]: http://wordpress.org/support/topic/i-want-to-disable-jquery-included-in-wordpress
 [3]: http://wordpress.org/support/profile/bazil749
 [4]: http://wordpress.org/support/topic/i-want-to-disable-jquery-included-in-wordpress#post-1193594
 [5]: http://blog.jquery.com/2010/11/11/jquery-1-4-4-release-notes/
 [6]: http://wordpress.org/extend/plugins/use-google-libraries/
 [7]: http://jqueryui.com/
 [8]: http://www.dojotoolkit.org/
 [9]: http://mootools.net/
 [10]: http://www.prototypejs.org/
 [11]: http://encosia.com/2008/12/10/3-reasons-why-you-should-let-google-host-jquery-for-you/
 [12]: #