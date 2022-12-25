---
title: Creating A WordPress Functionality Plugin
author: Tyler Longren
type: post
date: 2014-03-11T15:10:16+00:00
url: /creating-a-wordpress-functionality-plugin/
featured_image: /wp-content/uploads/2014/03/functionality.jpg
dsq_thread_id:
  - 2382753141
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - Internet
  - Open Source
  - opensource
  - plugin
  - plugins
  - poll
  - theme
  - themes
  - WordPress
  - wordpress-plugins
  - wordpress-themes

---
## Keep your customizations in place, like that driftwood up there {.subtitle}

A functionality plugin is a WordPress plugin that is specific to your site, and contains the additional functionality you need your site to have. This is a much better option than adding features to your theme&#8217;s **functions.php** file, because it allows you to change themes at will, yet keep your customizations via the plugin.

[WPCandy has a great write-up][1] on creating a functionality plugin and does a great job of explaining why you&#8217;d want to use one, and also what kind of things belong in a functionality plugin. Here&#8217;s one of my favorite pieces from that WPCandy article:

> To decide what belongs in a functions.php file and what belongs in a functionality plugin, think long term. Rather than thinking about how your website will look and behave this week, think about how it will look and behave five years from now. With few exceptions, I bet all of our sites will have new and upgraded themes in five years’ time.

If a feature is theme-specific, such as sidebars or menus, is **should go into your functions.php file**. If the feature interacts with content of _any type_, it **belongs in a functionality plugin**.

### Creating The Plugin

This piece is so easy, we&#8217;re essentially creating our own WordPress plugin. **First**, create a new folder called **functionality-plugin**. Create it inside the **plugins** folder for your WordPress site.

**Next**, we just need to create the PHP file and save it in the **functionality-plugin** folder. Your plugin needs to have some specific content in the comments at the top of the file for WordPress to recognize it as a plugin, you can see those in the functionality plugin example below. Our functionality plugin will load a JavaScript file that your site relies on ALL the time, no matter what theme is currently in use.

<pre class="lang:php decode:true " >&lt;?php
/*
Plugin Name: Tyler's Functionality Plugin
Description: Everything to run my site.
Version: 1.0
License: GPL
Author: Tyler Longren
Author URI: http://longren.io/
*/

function load_site_scripts() {
    // load javascript
    wp_enqueue_script( 'photo-service-script', 'http://thisphotoservice.com/script.js' );
 
}
add_action( 'wp_enqueue_scripts', 'load_site_scripts' );

?&gt;</pre>

So, with that, as long as this plugin is enabled, your site will always load that necessary JavaScript file, `http://thisphotoservice.com/script.js`.

You can safely use that code as a starting point for your own functionality plugin. Just make sure to save that code in the **functionality-plugin** folder.

The filename doesn&#8217;t matter, just make sure to save it with a `.php` extension. Navigate in your web browser to your WordPress Dashboard, go to Plugins, and enable your plugin just like you would any other plugin. **That&#8217;s it!**

Really, most of what I know about functionality plugins came from [Ryan Imel and his article at WPCandy][1], so a LOT of credit is owed to Ryan.

<div id="polls-20" class="wp-polls">
</div>

<div id="polls-20-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

There&#8217;s this plugin at WordPress.org, too, called [Functionality][2]. It&#8217;s essentially a plugin for creating a functionality plugin it looks like, but I&#8217;m really not sure. Anybody used it before? Comments are open below. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5965"
					data-ulike-nonce="372d71267a"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5965"></button><span class="count-box"></span>
  </div>
</div>

[][3]{.later-button-el}

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

 [1]: http://wpcandy.com/teaches/how-to-create-a-functionality-plugin/
 [2]: https://wordpress.org/plugins/functionality/
 [3]: #