---
title: Add Open Graph Protocol Markup to Any WordPress Theme
author: Tyler Longren
type: post
date: 2014-05-14T12:55:15+00:00
url: /add-open-graph-protocol-markup-to-your-wordpress-theme/
featured_image: /wp-content/uploads/2014/05/og.jpg
dsq_thread_id:
  - 2682665839
independent_publisher_primary_category:
  - WordPress
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - code
  - facebook
  - facebook open graph
  - Internet
  - open graph
  - opengraph
  - PHP
  - schema.org
  - structured data
  - themes
  - WordPress
  - wordpress-themes

---
## Rich objects in a social graphs {.subtitle}

When you share a link on Facebook, an image from the link is shown, usually. Sometimes, no image is displayed, as if Facebook couldn&#8217;t find a suitable image at the URL.

### Why?

Adding [Open Graph protocol][1] tags to your site will ensure that Facebook knows which image to use when someone shares a page on your website. Open Graph markup is similar to [schema.org markup][2]. Both allow you to define values for certain aspects of your website, as seen by other sites like Facebook, Twitter, and many other social media sites.

### How?

There&#8217;s a couple of ways we can do this. You can use a plugin, like [Open Graph Protocol Framework][3], or you can add Open Graph markup to your WordPress theme manually.

We&#8217;ll be covering how to add Open Graph markup to your theme manually. Especially useful for theme developers who want to build Open Graph protocol support into their themes.

The markup we&#8217;ll be adding can be seen in [this GitHub gist][4]:

<div class="oembed-gist">
  <noscript>
    View the code on <a href="https://gist.github.com/tlongren/e9e2316fa95b50cbed38">Gist</a>.
  </noscript>
</div>

Most of that should be pretty self-explanatory.

The `og:type` property is the only tag that needs explanation, as there&#8217;s only certain values that are valid. Most of the time, you&#8217;ll probably be setting the `og:type` property to `article` or `website`. A [list of other Open Graph protocol object types][5] can be found at the [Open Graph protocol site][5].

### The Code

Every Open Graph property will be set on-the-fly, depending on which post or page is being viewed or shared. To add the necessary markup, we need to use the [add_action][6] WordPress function inside your theme&#8217;s `functions.php` file. Here&#8217;s how I&#8217;ve been handing it:

<div class="oembed-gist">
  <noscript>
    View the code on <a href="https://gist.github.com/tlongren/de3f80c5f0b54a01e24f">Gist</a>.
  </noscript>
</div>

[Comments are open below][7], feel free to ask questions or tell me how wrong I am on one point or another. 🙂 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5922"
					data-ulike-nonce="f320672b83"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5922"></button><span class="count-box">1+</span>
  </div>
</div>

[][8]{.later-button-el}

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

 [1]: http://ogp.me/
 [2]: http://longren.io/add-schema-org-markup-to-any-wordpress-theme/
 [3]: http://wordpress.org/plugins/open-graph-protocol-framework/
 [4]: https://gist.github.com/tlongren/e9e2316fa95b50cbed38
 [5]: http://ogp.me/#types
 [6]: http://codex.wordpress.org/Function_Reference/add_action
 [7]: http://longren.io/add-open-graph-protocol-markup-to-your-wordpress-theme/#respond
 [8]: #