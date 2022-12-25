---
title: Add Infinite Scroll to Your WordPress Theme Using Jetpack
author: Tyler Longren
type: post
date: 2014-03-05T17:10:35+00:00
url: /add-infinite-scroll-to-your-wordpress-theme-using-jetpack/
featured_image: /wp-content/uploads/2014/03/jetpack-infinite-scroll.png
dsq_thread_id:
  - 2348545299
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - Internet
  - JavaScript
  - jetpack
  - jquery
  - Open Source
  - Personal
  - poll
  - themes
  - WordPress
  - wordpress-themes

---
 

## Scroll Forever, Or Until There&#8217;s No More Posts

It&#8217;s no secret I&#8217;m a big fan of [Jetpack][1]. A single plugin adds so many options, not only for end users, but for we developers too! An [excellent example would be infinite scroll][2].

Jetpack is a very popular plugin, so supporting Jetpack-specific features in your themes will end up just making your users _happier_. Kind of like an added bonus they didn&#8217;t realize they could use if they&#8217;re using your theme and Jetpack.

Infinite scroll is incredibly easy to add to &#8220;well-crafted&#8221; themes. The [Twenty Twelve theme][3] is a great example. Enabling infinite scroll is _slightly_ more complicated with not-so-well-crafted themes, but it&#8217;s still pretty easy.

## Enable Infinite Scroll in Well-Crafted Themes

Just add the following to your `functions.php` file.

<pre class="wp-block-preformatted">add_theme_support( 'infinite-scroll', array(
    'container' => 'content',
    'footer' => 'page',
) );</pre>

## Enable Infinite Scroll in Not-So-Well-Crafted Themes

### Activate Infinite Scroll

Add the following to the `functions.php` file for your theme.

<pre class="wp-block-preformatted">function mytheme_infinite_scroll_init() {
    add_theme_support( 'infinite-scroll', array(
        'container' => 'content',
        'render'    => 'mytheme_infinite_scroll_render',
        'footer'    => 'wrapper',
    ) );
}
add_action( 'init', 'rootdip_infinite_scroll_init' );</pre>

### Setup Function for the Render Parameter

The `render` parameter specifies a function, in this case, `mytheme_infinite_scroll_init`. That function uses the WordPress loop to load additional posts to be shown for infinite scrolling.

To hook this all up, add the following to your `functions.php` file.

<pre class="wp-block-preformatted">add_action( 'init', 'mytheme_infinite_scroll_init' );
function rootdip_infinite_scroll_render() {
    get_template_part( 'loop' );
}</pre>

In `mytheme_infinite_scroll_init`, the &#8216;loop&#8217; parameter value defines the file where your wordpress loop sits. It should be very basic and only contain markup and PHP you want to be included with every post. Have a look at the [loop.php file][4] from [Rootdip][5] for an example.

## That&#8217;s It

There&#8217;s more options that you can play with that are [described on the Jetpack Infinite Scroll page][2], such as styling specifics and JavaScript events.

That&#8217;s really all there is to it. With the above code you&#8217;ll have a working Jetpack Infinite Scroll in your WordPress theme. Whether you&#8217;ve got a well-crafted theme or not, you should be able to add infinite scroll via Jetpack fairly easily.

I&#8217;d suggest adding an option to your theme options to allow users to enable or disable Infinite Scroll.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5645"
					data-ulike-nonce="bd88724cba"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5645"></button><span class="count-box">5+</span>
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

 [1]: http://jetpack.me/
 [2]: http://jetpack.me/support/infinite-scroll/
 [3]: https://wordpress.org/themes/twentytwelve
 [4]: https://github.com/tlongren/rootdip/blob/master/loop.php
 [5]: http://www.longren.org/wordpress/rootdip/
 [6]: #