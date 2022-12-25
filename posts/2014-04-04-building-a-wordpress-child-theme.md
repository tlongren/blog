---
title: Building a WordPress Child Theme
author: Tyler Longren
type: post
date: 2014-04-04T19:44:21+00:00
url: /building-a-wordpress-child-theme/
featured_image: /wp-content/uploads/2014/04/wordpress-child-themes.png
dsq_thread_id:
  - 2586768715
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
independent_publisher_primary_category:
  - WordPress
tags:
  - Internet
  - Open Source
  - opensource
  - Personal
  - PHP
  - WordPress
  - wordpress-theme
  - wordpress-themes

---
 

## Make changes to your theme the correct way

Whenever I&#8217;m using a pre-built theme and need to make changes to it, I [create a child theme][1] and then make all changes to that child theme.

A child theme inherits features from it&#8217;s parent theme. This allows you to make modifications to the child theme without affecting the code in the parent theme, which allows the parent theme to be updated as normal, without causing your modifications to be lost.

### Benefits of using a child theme

  * If you modify an existing theme and it is updated, your changes will be lost. With a child theme, you can update the parent theme (which might be important for security or functionality) and still keep your changes.
  * It can speed up development time.
  * It’s a great way to get started if you are just learning WordPress theme development.

### Creating the Child Theme

Only one file is required when building a WordPress child theme, `style.css`. The only required lines in style.css are _Theme Name_ and _Template_. I typically use something like the following for my style.css file. Just set the _Template_ value to whatever the name of your parent theme is. In my case, it&#8217;s `independent-publisher`.

<pre class="wp-block-preformatted">Theme Name: longren.io
Theme URI: http://longren.io/
Author: Tyler Longren
Author URI: http://longren.io
Template: independent-publisher
Description: Independent Publisher is beautiful reader-focused WordPress theme, for you. Clean, responsive, and mobile-ready, it gets out of your way and lets you share what you create. Full support for all Post Formats. This theme is ideal for both single-author and multi-author blogs.
Version: 1.0
License: GNU GPLv3
License URI: http://www.gnu.org/copyleft/gpl.html</pre>

### Example Child Theme GitHub Repository

I put together a simple child theme example, [it&#8217;s available on GitHub][2].

Feel free to use it as a base for your child themes. It&#8217;s setup to include the parent theme CSS, child theme CSS, and the [Font Awesome CSS][3]. If you need help, you can ask in the comments at this post, or [create an issue at the GitHub repository][4].

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="6267"
					data-ulike-nonce="7a4e220fcb"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_6267"></button><span class="count-box"></span>
  </div>
</div>

[][5]{.later-button-el}

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

 [1]: https://codex.wordpress.org/Child_Themes
 [2]: https://github.com/tlongren/wordpress-child-example
 [3]: http://fortawesome.github.io/Font-Awesome/icons/
 [4]: https://github.com/tlongren/wordpress-child-example/issues
 [5]: #