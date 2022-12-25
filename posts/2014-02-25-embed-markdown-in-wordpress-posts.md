---
title: Embed MarkDown in WordPress Posts
author: Tyler Longren
type: post
date: 2014-02-25T17:45:26+00:00
url: /embed-markdown-in-wordpress-posts/
featured_image: /wp-content/uploads/2014/02/inline-markdown-crushed.png
dsq_thread_id:
  - 2315278476
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
independent_publisher_primary_category:
  - WordPress
tags:
  - GitHub
  - Internet
  - markdown
  - Open Source
  - Personal
  - PHP
  - plugin
  - plugins
  - WordPress

---
## Easily embed markdown into WordPress posts and pages. {.subtitle}

There&#8217;s lots of [plugins to enable your entire post to be composed of Markdown][1], but what if you only want a piece of your post to be in Markdown? I shortcode sure would come in handy.

This is where the [Inline Markdown plugin][2] comes in to play. Just write your WordPress post as usual, and wrap any Markdown content in the <span class="lang:default decode:true  crayon-inline " ></p> 

<p>
  </span> shortcode.
</p>

<p>
  As an example, here&#8217;s a portion of the README from my Rootdip WordPress theme, that&#8217;s written in Markdown. Inline Markdown is an excellent tool for displaying entire README&#8217;s or portions of them from GitHub repos.
</p>

<h2>
  <strong>The <em>md shortcode</em> starts immediately following this line:</strong><br /> [md]Other Considerations
</h2>

<p>
  A majority of the images included in RootDip are from the <a href="http://somerandomdude.com/projects/iconic/" title="Iconic Icons!">iconic icon set</a> by <a href="http://somerandomdude.com/" title="Some Random Dude">P.J. Onori</a>. Images from Iconic are the tag, sticky post identifier, link post format identifier, status post format identifier, quote post format identifier and left and right arrows. I will likely use more images from Iconic as I add additional features/post formats to RootDip.
</p>

<h2>
  How To Contribute
</h2>

<ol>
  <li>
    Fork it
  </li>
  <li>
    Create your feature branch (<code>git checkout -b my-new-feature</code>)
  </li>
  <li>
    Commit your changes (<code>git commit -am 'Add some feature'</code>)
  </li>
  <li>
    Push to the branch (<code>git push origin my-new-feature</code>)
  </li>
  <li>
    Create new Pull Request
  </li>
</ol>

<p>
  <strong>And that&#8217;s it</strong>, end of the <em>md</em> shortcode is on the line above. I used the md shortcode like so to achieve that:
</p>

<pre><code>&lt;h2>Other Considerations&lt;/h2>
&lt;p>A majority of the images included in RootDip are from the &lt;a href="http://somerandomdude.com/projects/iconic/" title="Iconic Icons!">iconic icon set&lt;/a> by &lt;a href="http://somerandomdude.com/" title="Some Random Dude">P.J. Onori&lt;/a>. Images from Iconic are the tag, sticky post identifier, link post format identifier, status post format identifier, quote post format identifier and left and right arrows. I will likely use more images from Iconic as I add additional features/post formats to RootDip.&lt;/p>
&lt;h2>How To Contribute&lt;/h2>
&lt;ol>
&lt;li>Fork it&lt;/li>
&lt;li>Create your feature branch (&lt;code>git checkout -b my-new-feature</code>)&lt;/li>


<li>
  Commit your changes (<code>git commit -am 'Add some feature'</code>)
</li>


<li>
  Push to the branch (<code>git push origin my-new-feature</code>)
</li>


<li>
  Create new Pull Request
</li>
&lt;/ol>&lt;/code></pre>

<p>
  Pretty easy to do and really useful for embedding markdown from GitHub readme&#8217;s directly in your WordPress posts.
</p>

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5392"
					data-ulike-nonce="42d11ebb5b"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5392"></button><span class="count-box"></span>
  </div>
</div>

<p>
  <a href='#' class='later-button-el'></a>
</p>

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

 [1]: http://wordpress.org/plugins/wp-markdown/screenshots/
 [2]: http://wordpress.org/plugins/inline-markdown/