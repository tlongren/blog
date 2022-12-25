---
title: Loading Scripts in WordPress Themes and Child Themes, Quickly
author: Tyler Longren
type: post
date: 2014-03-04T05:54:50+00:00
url: /loading-scripts-in-wordpress-quickly/
featured_image: /wp-content/uploads/2014/03/js.png
dsq_thread_id:
  - 2355941926
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - how-to
  - Internet
  - Open Source
  - opensource
  - PHP
  - themes
  - tutorials
  - WordPress
  - wordpress-themes

---
Here&#8217;s how I load scripts and styles in WordPress themes, in functions.php.

<pre class="lang:php decode:true " >function load_scripts() {
    // load styles
    wp_enqueue_style( 'custom-css-1', get_stylesheet_directory_uri() . '/css/custom-css-1.css' );
    wp_enqueue_style( 'my-secret-script-css', get_stylesheet_directory_uri() . '/css/my-secret-script.css' );


    // load javascript
    wp_enqueue_script( 'my-secret-script', get_stylesheet_directory_uri() . '/js/my-secret-script.js' );

}
add_action( 'wp_enqueue_scripts', 'load_scripts' );</pre>

The above code would load up two css files, `custom-css-1.css` and `my-secret-script.css`. It would also load one JavaScript file, `my-secret-javascript.js`.

[This post by [Brian Krogsgard][1] at [WPCandy][2] describes the proper way][3] of loading scripts, using `wp_register_script`, as it takes dependencies into consideration and allows loading of scripts by their defined name. However, I think the `wp_register_script` methodology is lengthier and a bit more difficult to read, mostly due to the dependency stuff.

However, _you do need to take dependencies into consideration_ if you&#8217;re using a JavaScript library, like [jQuery][4].

`wp_register_style` should also be used to load styles with dependencies. This [article at Tuts+ has a very good description and examples][5] on loading CSS stylesheets using `wp_register_style` and `wp_enqueue_style`.

You should also be aware of the differences when authoring themes and plugins, which Brian also explains in [his post on WPCandy][3]. That mostly involves one WordPress function out for another.

Let me know if you run into any issues, comments are open! 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5754"
					data-ulike-nonce="f159239d66"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5754"></button><span class="count-box"></span>
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

 [1]: http://wpcandy.com/author/briank/
 [2]: http://wpcandy.com
 [3]: http://wpcandy.com/teaches/how-to-load-scripts-in-wordpress-themes/
 [4]: http://jquery.com/
 [5]: http://code.tutsplus.com/articles/how-to-include-javascript-and-css-in-your-wordpress-themes-and-plugins--wp-24321
 [6]: #