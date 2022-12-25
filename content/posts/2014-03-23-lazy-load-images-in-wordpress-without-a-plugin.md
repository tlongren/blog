---
title: Lazy Load Images in WordPress Without A Plugin
author: Tyler Longren
type: post
date: 2014-03-23T12:49:37+00:00
draft: true
url: /?p=5726
featured_image: /wp-content/uploads/2014/03/unveil-e1395524304526.png
dsq_thread_id:
  - 2487756470
tags:
  - image
  - Internet
  - JavaScript
  - jquery
  - lazy load
  - Open Source
  - opensource
  - PHP
  - plugins
  - WordPress
  - wordpress-plugin
  - wordpress-plugins

---
## Possibly lighter image lazy loading {.subtitle}

We&#8217;ll be using [Unveil.js][1] to do this, from [Luís Almeida][2]. Unveil.js [can be found on Github][3]. A demo of the [can be found right on the Unveil.js site][1].

For those not familiar with image lazy loading, here&#8217;s how [Uneil.js][1] describes itself on it&#8217;s homepage:

> This plugin is very useful and it boosts performance delaying loading of images in long web pages because images outside of viewport (visible part of web page) won&#8217;t be loaded until the user scrolls to them.
> 
> Lazy Load has some cool options such as custom effects, container, events or data attribute. If you&#8217;re not gonna use any of them you can reduce the file size by leaving just the essential code to show the images.
> 
> That&#8217;s what I did and this is my lightweight version of Lazy Load with support for serving high-resolution images to devices with retina displays &#8211; less than 1k.

This should be pretty simple since we know how to [quickly load up scripts for our WordPress themes][4]. First thing you&#8217;ll want to do is edit your **functions.php** file.

We&#8217;ll be using [Unveil.js from cdnjs.com][5] for this example, so you won&#8217;t need to download the JavaScript. The latest version as of this post, 1.3.0, is on [cdnjs.com][6].

Now, create a new file named **load_unveil.js**, add this to it, and save it to the same directory your themes javascript files are stored in, usually **js**:

<pre class="lang:js decode:true " >jQuery(document).ready(function($) {
  $("img").unveil();
});</pre>

That tells Unveil.js which images to lazily load. The above example lazily loads all <span class="lang:xhtml decode:true  crayon-inline " ><img></span> tags within a <span class="lang:css decode:true  crayon-inline " >#content</span> container. Most WordPress themes are built using a <span class="lang:css decode:true  crayon-inline " >#content</span> container.

Make sure that jQuery is loading in your theme before you include the following code in **functions.php**, or none of this will work.

### Putting It All Together

We&#8217;ll be using the WordPress function [add_action][7] to load the JavaScript up. We just load our jQuery plugin, then our **load_lazyload.js**, and that&#8217;s basically it.

Put this in your **functions.php** file or in [your functionality plugin][8], which would make an awesome home for this.

<pre class="lang:php decode:true " >function load_lazyload() {
    // load javascript
    wp_enqueue_script( 'jquery_lazyload', get_stylesheet_directory_uri() . '/js/jquery.lazyload.min.js' ); // jQuery plugin
    wp_enqueue_script( 'our_lazyload', get_stylesheet_directory_uri() . '/js/load_lazyload.js' ); // Our jquery_lazyload javascript code

}
add_action( 'wp_enqueue_scripts', 'load_lazyload' );</pre>

That&#8217;s it! [Unveil.js][1] should now be handling image loading.

If it doesn&#8217;t seem to be working, make sure to check that all the necessary javascript files are being loaded. Use developer tools in any of the major web browsers to determine if they&#8217;re all being loaded. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5726"
					data-ulike-nonce="09907b5257"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5726"></button><span class="count-box"></span>
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

 [1]: http://luis-almeida.github.io/unveil/
 [2]: https://github.com/luis-almeida
 [3]: https://github.com/luis-almeida/unveil/
 [4]: http://longren.io/loading-scripts-in-wordpress-quickly/
 [5]: http://cdnjs.com/libraries/unveil/
 [6]: http://cdnjs.com
 [7]: https://codex.wordpress.org/Function_Reference/add_action
 [8]: http://longren.io/creating-a-wordpress-functionality-plugin/
 [9]: #