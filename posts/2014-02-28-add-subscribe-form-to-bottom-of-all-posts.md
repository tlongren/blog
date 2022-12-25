---
title: 'Add Jetpack Subscribe Form To Bottom of All WordPress Posts & Pages'
author: Tyler Longren
type: post
date: 2014-02-28T16:15:25+00:00
url: /add-subscribe-form-to-bottom-of-all-posts/
featured_image: /wp-content/uploads/2014/02/jetpack-crushed.png
dsq_thread_id:
  - 2323229181
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - Internet
  - jetpack
  - Open Source
  - Personal
  - PHP
  - poll
  - subscribe
  - themes
  - WordPress
  - wordpress-theme
  - wordpress-themes

---
You may have noticed I&#8217;ve added subscribe widgets at the end of every post, right below the related articles. It&#8217;s really simple to do, and comes built-in with the [Jetpack WordPress Plugin][1].

First, make sure you&#8217;re using a child theme so you&#8217;re not changing the core code of your theme, as your changes will be lost on updates. You can read about creating a child theme [here at the WordPress Codex][2].

### 1. Register New Sidebar

First, add this to your `functions.php` file. It will [register a new sidebar][3] called _Subscribe In Page_.

<pre class="lang:php decode:true " >register_sidebar( array(
    'name' =&gt; 'Subscribe in page',
    'id' =&gt; 'subscribe-in-page',
    'before_widget' =&gt; '&lt;div id="subscribe"&gt;',
    'after_widget' =&gt; '&lt;/div&gt;',
    'before_title' =&gt; '&lt;h3&gt;',
    'after_title' =&gt; '&lt;/h3&gt;'
) );</pre>

### 2. Call Our New Sidebar

Now, in your [WordPress loop][4], find something like <span class="lang:php decode:true  crayon-inline " ><?php the_content(); ?></span>. Here&#8217;s what my `the_contenet()` call looks like:

<pre class="lang:php decode:true " >&lt;div class="entry-content" itemprop="mainContentOfPage"&gt;
    &lt;?php the_content(); ?&gt;
    &lt;?php wp_link_pages( array( 'before' =&gt; '&lt;div class="page-links-next-prev"&gt;', 'after' =&gt; '&lt;/div&gt;', 'nextpagelink' =&gt; '&lt;button class="next-page-nav"&gt;' . __( 'Next page &rarr;', 'independent_publisher' ) . '&lt;/button&gt;', 'previouspagelink' =&gt; '&lt;button class="previous-page-nav"&gt;' . __( '&larr; Previous page', 'independent_publisher' ) . '&lt;/button&gt;', 'next_or_number' =&gt; 'next' ) ); ?&gt;
    &lt;?php wp_link_pages( array( 'before' =&gt; '&lt;div class="page-links"&gt;' . __( 'Pages:', 'independent_publisher' ), 'after' =&gt; '&lt;/div&gt;' ) ); ?&gt;
&lt;/div&gt;
&lt;!-- .entry-content --&gt;</pre>

Notice there&#8217;s a couple functions after <span class="lang:php decode:true  crayon-inline " >the_content()</span>, this is normal and will vary from theme to theme. Any plugins you&#8217;ve got set to appear below your post will be shown, and then the subscription form will be shown.

### 4. Add Your Jetpack Subscribe Widget

Just like adding a normal widget. Go to **Appearances**, and then **Widgets**. You should see an area titled **Subscribe In Page**. Drag the _Blog Subscriptions (JetPack)_ widget into the Subscribe In Page sidebar area. Configure it, save it.

### 5. Add The Sidebar To The Theme

To add the Jetpack subscription form, add <span class="lang:php decode:true  crayon-inline " ><?php dynamic_sidebar( &#8216;subscribe-in-page&#8217; ); ?></span>, which calls our custom sidebar, to your loop. It should go somewhere under `the_content()` if you want it to show at the end of the post. If you want it at the beginning, add <span class="lang:php decode:true  crayon-inline " ><?php dynamic_sidebar( &#8216;subscribe-in-page&#8217; ); ?></span> before `the_content()`.

### You&#8217;re Done!

And that&#8217;s really all there is to adding a subscribe form to the end of each post. You can also add the same subscribe form in the sidebar, like I have at longren.org. As a note, the [Jetpack][1] plugin is packed full of functionality. Chances are good that you&#8217;ll find more Jetpack modules to use, other than the [Subscriptions module][5].

<div id="polls-19" class="wp-polls">
</div>

<div id="polls-19-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5452"
					data-ulike-nonce="0686865b28"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5452"></button><span class="count-box">2+</span>
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

 [1]: http://jetpack.me/
 [2]: https://codex.wordpress.org/Child_Themes
 [3]: http://codex.wordpress.org/Function_Reference/register_sidebar
 [4]: https://codex.wordpress.org/The_Loop
 [5]: http://jetpack.me/support/subscriptions/
 [6]: #