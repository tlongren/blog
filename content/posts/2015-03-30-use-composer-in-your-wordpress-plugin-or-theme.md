---
title: Use Composer in Your WordPress Plugin or Theme
author: Tyler Longren
type: post
date: 2015-03-30T12:00:20+00:00
url: /use-composer-in-your-wordpress-plugin-or-theme/
featured_image: /wp-content/uploads/2015/03/wordpress-composer.png
independent_publisher_primary_category:
  - WordPress
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
dsq_thread_id:
  - 3638772763
tags:
  - how-to
  - Internet
  - Open Source
  - Personal
  - PHP
  - plugins
  - themes
  - tools
  - tutorials
  - WordPress
  - wordpress-plugins
  - wordpress-themes

---
## Simple Tutorial Showing How To Use Composer in Your WordPress Plugin or Theme

I love [Composer][1]. It just makes including libraries or scripts in your app incredibly easy. So easy that it&#8217;s stupid not to use it (in many, if not most cases).

The number of libraries/scripts available on [Packagist][2] is astounding, all of which can be included in your plugin with Composer. Packagist is the main Composer repository. It basically aggregates all types of PHP packages that can be installed via Composer.

I&#8217;d never used Composer with a proprietary WordPress plugin before. The plugin is for a client so it&#8217;ll never be available to the public.

Here&#8217;s the steps I took to make this WordPress plugin compatible with Composer so that I can easily bring in third-party libraries.

We&#8217;ll be using [mailgun-php][3] throughout this example, as the plugin that inspired this post uses [Mailgun][4] to send all sorts of emails.

### 1. First, install composer on your server.

I install Composer globally, like so: 

<pre class="EnlighterJSRAW" data-enlighter-language="shell" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">curl -sS https://getcomposer.org/installer | php&lt;br>sudo mv composer.phar /usr/local/bin/composer</pre>

### 2. Add Mailgun as a dependency.

<pre class="EnlighterJSRAW" data-enlighter-language="shell" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">cd /path/to/plugin/
composer require mailgun/mailgun-php:~1.7.2</pre>

### 3. Check your composer.json file.

We&#8217;re including [Mailgun][5] and [guzzle][6] from Packagist. Your composer.json file should look similar to the example below.  
<figure class="wp-block-embed is-type-rich is-provider-embed-handler">

<div class="wp-block-embed__wrapper">
  <div class="oembed-gist">
    <noscript>
      View the code on <a href="https://gist.github.com/tlongren/209fb9c23a9563c94236">Gist</a>.
    </noscript>
  </div>
</div></figure> 

### 4. Tell composer to install Mailgun.

<pre class="wp-block-preformatted">tyler@yourmachine:~/path/to/plugin$ composer install</pre>

### 5. Autoload Our Mailgun Classes in Our Plugin.

The following should go in your `plugin-name.php` file, before any other PHP code. 

<pre class="EnlighterJSRAW" data-enlighter-language="php" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">&lt;?php
require 'vendor/autoload.php';
use MailgunMailgun;</pre>

You can now use Mailgun in your WordPress plugin or theme, some basic [examples of using Mailgun can be found on GitHub][3] and in their [official documentation][7].

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7942"
					data-ulike-nonce="2eeb6cce0b"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7942"></button><span class="count-box">2+</span>
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

 [1]: https://getcomposer.org/
 [2]: https://packagist.org/
 [3]: https://github.com/mailgun/mailgun-php
 [4]: http://mailgun.com/
 [5]: https://packagist.org/packages/mailgun/mailgun-php
 [6]: https://packagist.org/packages/guzzle/guzzle
 [7]: https://documentation.mailgun.com/api_reference.html
 [8]: #