---
title: Basic Routing in PHP with AltoRouter
author: Tyler Longren
type: post
date: 2014-02-16T19:57:06+00:00
url: /basic-routing-in-php-with-altorouter/
featured_image: /wp-content/uploads/2014/02/PHP_Logo.png
dsq_thread_id:
  - 2276465660
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
independent_publisher_primary_category:
  - PHP
tags:
  - apache
  - code
  - GitHub
  - how-to
  - Internet
  - Open Source
  - PHP
  - tools
  - tutorials

---
## Routing in PHP using AltoRouter

I&#8217;ve been using [AltoRouter][1] for help with building simple API&#8217;s. A full framework (even a micro-framework), like [Slim][2], is usually overkill for my needs, and often, any kind of routing class is overkill. A .htaccess file with the proper rewrite rules will usually suffice.

When I do need a bit more control than a .htaccess file provides, I usually go with AltoRouter. AltoRouter is really easy to use.

First thing to do when using AltoRouter, or pretty much any PHP routing class/script, is to direct all requests to index.php. We do this with a .htaccess file. Here&#8217;s the .htaccess file I usually use with a project using AltoRouter:<figure class="wp-block-embed is-type-rich is-provider-embed-handler">

<div class="wp-block-embed__wrapper">
  <div class="oembed-gist">
    <noscript>
      View the code on <a href="https://gist.github.com/tlongren/9038802">Gist</a>.
    </noscript>
  </div>
</div></figure> 

That will direct all requests to your site to index.php. Inside index.php is where we setup AltoRouter, define our routing rules, and specify any parameters that we want to capture. A basic example of an index.php file using AltoRouter can be seen below.  
<figure class="wp-block-embed is-type-rich is-provider-embed-handler">

<div class="wp-block-embed__wrapper">
  <div class="oembed-gist">
    <noscript>
      View the code on <a href="https://gist.github.com/tlongren/9038883">Gist</a>.
    </noscript>
  </div>
</div></figure> 

Lines 10-15 are just standard routes being setup, we could easily do this with a .htaccess file. The next block, with the &#8220;Special&#8221; comment title, is a little more involved. But only because we&#8217;re passing a parameter or two to our PHP controller.

When I say PHP controller, I&#8217;m referencing the third parameter in the AltoRouter map() method. The **first** parameter is the HTTP request method, usually either **GET** or **POST**. The **second** parameter is the route we want to watch for. The **third** parameter is the controller, or the PHP file that we want when the route from parameter two is matched. And the **fourth** parameter is just a unique name for that route.

If you&#8217;re using named parameters in your routes, like you see being done on **lines 18 and 19** in the **index.php gist**, you&#8217;re going to want to access them within your controller. Notice the very end of the index.php gist, specifically, everything below the _/\* Match the current request \*/_ comment. That&#8217;s where we&#8217;re doing the actual matching, if the current URL matches a defined route, then we require the controller.

Before that though, we&#8217;re actually setting the $match variable. Since we&#8217;re setting $match before including our controller, $match should be available for use within our controller, which is awesome!

Say we&#8217;re charging a customer, and this is done by hitting /charge/the\_customer\_id/, where **the\_customer\_id** is an actual customer ID. In our controller, charge.php, we can access **the\_customer\_id** named parameter as seen below. It&#8217;s available in `$match['params']['customer_id']`.<figure class="wp-block-embed is-type-rich is-provider-embed-handler">

<div class="wp-block-embed__wrapper">
  <div class="oembed-gist">
    <noscript>
      View the code on <a href="https://gist.github.com/tlongren/9039329">Gist</a>.
    </noscript>
  </div>
</div></figure> 

You can use all sorts of limits on your named parameters, like integer matching, alphanumeric matching, and even hexadecimal character matching. A useful list of named parameter limits and some examples can be seen in the [AltoRouter readme][1]. Comments are open, so please let me know if I&#8217;ve missed something or am just totally off base somewhere. Thanks!!

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5150"
					data-ulike-nonce="629930a7ae"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image image-unlike wp_ulike_btn_is_active wp_likethis_5150"></button><span class="count-box">8+</span>
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

 [1]: https://github.com/dannyvankooten/AltoRouter
 [2]: http://slimframework.com/
 [3]: #