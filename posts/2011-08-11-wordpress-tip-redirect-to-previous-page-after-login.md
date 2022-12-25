---
title: 'WordPress Tip: Redirect to Previous Page After Login'
author: Tyler Longren
type: post
date: 2011-08-11T16:19:19+00:00
url: /wordpress-tip-redirect-to-previous-page-after-login/
views:
  - 298
dsq_thread_id:
  - 1385918028
primary_category:
  - WordPress
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
independent_publisher_primary_category:
  - WordPress
tags:
  - code
  - howto
  - Internet
  - Personal
  - tips
  - WordPress

---
 

I work for a group of newspapers here in Iowa. We recently started moving these sites to WordPress. Site visitors must be logged in to view stories. They can see all the stories on the front page, but when they click through to a single story, they see a login form in place of the post/story content.

I needed to redirect users back to the page they were viewing after logging in. So, if a user was viewing a story called &#8220;Look at me now&#8221;, they&#8217;d need to be redirected back to that story after logging in.

To achieve this redirect to previous page after login, add the following code to the **functions.php** file for your theme:  
<figure class="wp-block-embed">

<div class="wp-block-embed__wrapper">
  <div class="oembed-gist">
    <noscript>
      View the code on <a href="https://gist.github.com/tlongren/ffea6b1f1339844e5ddd2cd87044a8ea">Gist</a>.
    </noscript>
  </div>
</div></figure> 

I looked at [a number of plugins][1] to do this, but none seemed to offer this functionality.

A bit of searching on Google [yielded this post at Taproot Creative][2]. I modified the code on that post to set the redirect location to the referring page, and that was it!

Now users are redirected back to the story/post they originated from.

If you use a [functionality plugin, which you really should][3], it&#8217;d make an ideal home for this snippet of code. So if you can, drop it in a [functionality plugin][3] instead of the `functions.php` file for your theme.

### This Doesn&#8217;t Work!

For the code above to work, your login form must be embedded in one of you theme&#8217;s templates, or in a post or page.

If you&#8217;re providing users a &#8220;Login&#8221; button that takes them to the default login page (_wp-login.php_), this won&#8217;t work for you, users will be sent to the WordPress dashboard instead of the page they were at before hitting _wp-login.php_.

If the code above doesn&#8217;t work (ie: users are logging in at wp-login.php), the code below will allow you to define a page to redirect users to after login:  
<figure class="wp-block-embed is-type-rich is-provider-embed-handler">

<div class="wp-block-embed__wrapper">
  <div class="oembed-gist">
    <noscript>
      View the code on <a href="https://gist.github.com/tlongren/ffea6b1f1339844e5ddd2cd87044a8ea">Gist</a>.
    </noscript>
  </div>
</div></figure> 

The example above will redirect users (including administrators) to _/members/_, and uses the [home_url() WordPress function][4]. So, if I were using this here, users would be redirected to <https://longren.io/about/>.

If you want to redirect users based on their role, like redirecting Administrators to the dashboard like normal, check out the example provided in the [login_redirect filter documentation][5].

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2957"
					data-ulike-nonce="5011a98143"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2957"></button><span class="count-box">4+</span>
  </div>
</div>

[][6]{.later-button-el}

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

 [1]: http://wordpress.org/extend/plugins/search.php?q=login+redirect&sort=
 [2]: http://taprootcreative.com/2010/12/wordpress-user-controlled-login-redirect/
 [3]: http://longren.io/creating-a-wordpress-functionality-plugin/
 [4]: http://codex.wordpress.org/Function_Reference/home_url
 [5]: http://codex.wordpress.org/Plugin_API/Filter_Reference/login_redirect
 [6]: #