---
title: 'Looking Ahead To WordPress 3.9: HTML5 Galleries'
author: Tyler Longren
type: post
date: 2014-03-17T11:00:43+00:00
url: /looking-ahead-to-wordpress-3-9-html5-galleries/
featured_image: /wp-content/uploads/2014/03/html5-gallery.png
dsq_thread_id:
  - 2439220781
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - Internet
  - Open Source
  - PHP
  - WordPress
  - wordpress-theme
  - wordpress-themes

---
## HTML5 In Your Galleries {.subtitle}

In WordPress 3.9, we&#8217;ll be able to [declare HTML5 support][1] for our galleries! [ThemeShaper has an excellent article][2] detailing HTML5 galleries in the upcoming WordPress 3.9.

According to the [ThemeShaper article][2], this is how it&#8217;ll work:

> Once a theme declared support, the definition list elements will be replaced by <span class="lang:default decode:true  crayon-inline " ><figure></span> and <span class="lang:default decode:true  crayon-inline " ><figcaption></span> for better semantics. If you decide to not only adopt this new feature but also maintain backwards compatibility, then there are two ways to achieve that:

The two options they mention to maintain backwards compatibility are:

  1. Style the new elements and add CSS selectors for the traditional definition list elements. That&#8217;s what ThemeShaper [did for the _s][3] starter theme.
  2. Filter the shortcode attributes and override the tag parameters. Since the shortcode\_atts\_gallery filter was introduced in 3.6, you’ll be backwards compatible with the latest two versions.

For more details on option one, [see how ThemeShaper handled it][3]. If you went with option two, you&#8217;d need to add this to your theme&#8217;s **functions.php** file:

<pre class="lang:php decode:true " >function prefix_gallery_atts( $atts ) {
    $atts['itemtag']    = 'figure';
    $atts['icontag']    = 'div';
    $atts['captiontag'] = 'figcaption';
 
    return $atts;
}
add_filter( 'shortcode_atts_gallery', 'prefix_gallery_atts' );</pre>

This post is primarily targeted towards people who are developing custom themes, available publicly or not. Most of the themes I develop are private and are used for one specific client&#8217;s site.

Not the best fit for inclusion in a functionality plugin. I suppose you could, only if you have no other choices, which you do. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="6160"
					data-ulike-nonce="03e1d191bc"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_6160"></button><span class="count-box"></span>
  </div>
</div>

[][4]{.later-button-el}

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

 [1]: https://core.trac.wordpress.org/changeset/27302
 [2]: http://themeshaper.com/2014/03/04/html5-galleries-in-wordpress-3-9/
 [3]: https://github.com/Automattic/_s/commit/5de96cdb729f3cfc21c117df2a298f49e7408d0b
 [4]: #