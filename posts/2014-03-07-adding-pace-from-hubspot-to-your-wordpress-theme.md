---
title: Adding Pace From HubSpot To Your WordPress Theme
author: Tyler Longren
type: post
date: 2014-03-07T17:33:24+00:00
url: /adding-pace-from-hubspot-to-your-wordpress-theme/
featured_image: /wp-content/uploads/2014/03/pace.png
dsq_thread_id:
  - 2349698706
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - GitHub
  - Internet
  - JavaScript
  - Open Source
  - opensource
  - themes
  - WordPress
  - wordpress-themes

---
[Pace.js][1], from [HubSpot][2], is pretty cool. It&#8217;s a page load progress bar that usually sits at the top of your website. The Minimial theme for Pace, which I like the best, gets hidden by the WordPress admin bar if you have it enabled. There&#8217;s a few different themes though, most work just fine with the WordPress admin bar.

HubSpot describes Pace better than I can.

> Include pace.js and a CSS theme of your choice, and you get a beautiful progress indicator for your page load and ajax navigation.
> 
> No need to hook into any of your code, progress is detected automatically.

Instead of downloading pace.js, I like to use [cdnjs][3] for this type of thing, [here&#8217;s pace.js on cdnjs.com][4].

In your `functions.php` file, just call the cdnjs file instead of a local file. You will, however, have to host the Pace theme CSS locally, which is usually tiny, unless you choose one of the more animated themes. I personally like the _Center Simple_ theme the best.

[<img loading="lazy" src="https://i2.wp.com/longren.org/wp-content/uploads/2014/03/pace-styles-300x271.png?resize=300%2C271" alt="Pace Themes" width="300" height="271" class="aligncenter size-medium wp-image-5714" srcset="https://i1.wp.com/www.longren.io/wp-content/uploads/2014/03/pace-styles.png?resize=300%2C271&ssl=1 300w, https://i1.wp.com/www.longren.io/wp-content/uploads/2014/03/pace-styles.png?resize=1024%2C927&ssl=1 1024w, https://i1.wp.com/www.longren.io/wp-content/uploads/2014/03/pace-styles.png?w=1050&ssl=1 1050w" sizes="(max-width: 300px) 100vw, 300px" data-recalc-dims="1" />][5]

The `wp_enqueue_style()` call below loads `/css/pace.css` from your theme&#8217;s stylesheet directory. That&#8217;s the file that should contain the CSS provided by the Pace theme download.

<pre class="lang:php decode:true " >/**
* load_scripts
*
* load up css and javascript for Pace.js
*/
function load_scripts() {
    // load styles
    wp_enqueue_style( 'pace-css', get_stylesheet_directory_uri() . '/css/pace.css' ); // Center Simple Theme CSS

    // load javascript
    wp_enqueue_script( 'pace', 'http://cdnjs.cloudflare.com/ajax/libs/pace/0.4.17/pace.min.js' ); // pace.min.js
}
add_action( 'wp_enqueue_scripts', 'load_scripts' );</pre>

If your `functions.php` file already contains a `add_action( 'wp_enqueue_scripts', 'load_scripts' )`, find the function it calls, and add `wp_enqueue_style` and `wp_enqueue_script` there instead of making a new function like the example above.

This is more for theme developers to build into their themes as options and such, so if you&#8217;re a regular WordPress user you&#8217;d be better served by a functionality plugin. Essentially a plugin that you always have activated that adds all the necessary extra elements of the site, like the Pure JavaScript and CSS.

I&#8217;ll show how to create your own functionality plugin within the next few posts/days. If you want notified of when exactly it&#8217;s posted, subscribe below. Look for the **Get New Posts via E-Mail** heading.

**Update:** There&#8217;s [a plugin to do this][6], too. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5701"
					data-ulike-nonce="4ab917aedf"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5701"></button><span class="count-box"></span>
  </div>
</div>

[][7]{.later-button-el}

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

 [1]: http://github.hubspot.com/pace/docs/welcome/
 [2]: http://github.hubspot.com/
 [3]: http://cdnjs.com/
 [4]: http://cdnjs.com/libraries/pace/
 [5]: https://i0.wp.com/longren.org/wp-content/uploads/2014/03/pace-styles.png
 [6]: https://wordpress.org/plugins/wp-pace/
 [7]: #