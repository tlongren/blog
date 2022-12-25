---
title: Add HTML To The End of Every WordPress Post
author: Tyler Longren
type: post
date: 2014-03-12T16:15:27+00:00
url: /add-html-to-the-end-of-every-wordpress-post/
featured_image: /wp-content/uploads/2014/03/HTML.jpg
dsq_thread_id:
  - 2356021801
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - Internet
  - Open Source
  - opensource
  - PHP
  - plugins
  - themes
  - WordPress
  - wordpress-plugins
  - wordpress-themes

---
 

## Great for signup forms or affiliate links

I don&#8217;t place the DigitalOcean affiliate link manually at the end of each post. That&#8217;s because it&#8217;s super easy to do with `add_filter('the_content')`.

### Add The Message, With or Without HTML

<pre class="wp-block-preformatted">function add_post_bottom_content($content){

    $html = '&lt;span class="post-footer-message"&gt;&lt;a href="http://oursponsor.com" target="_blank"&gt;Thanks to our sponsor for the generous donation!&lt;/a&gt;&lt;/span&gt;';

    if( !is_page( ) && isset($html) ) {

        return $content . $html;

    } else {

        return $content;

    }

}

add_filter('the_content', 'add_post_bottom_content');</pre>

To disable the content, just empty the `$html` variable . 

<pre class="wp-block-preformatted">$html='';</pre>

The anchor tag is wrapped in a `span` with a class of `post-footer-message`. You&#8217;ll want to style your message with that, rename the classes if you want, just stay consistent with the naming.

Some basic styling, with no underline on hover:

<pre class="wp-block-preformatted">span.do_link a:hover {
  font-style:none;
}</pre>

As long as you have some basic CSS knowledge, you&#8217;ll be able to apply all the styling you need. Just remember to add your CSS to your child theme&#8217;s `style.css` file, or load [up the custom CSS file][1].

The code in this post can go in your theme&#8217;s **functions.php** file or in your [WordPress functionality plugin][2].

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5746"
					data-ulike-nonce="c7be0ebb96"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5746"></button><span class="count-box">3+</span>
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

 [1]: http://longren.org/loading-scripts-in-wordpress-quickly/
 [2]: http://longren.io/creating-a-wordpress-functionality-plugin/
 [3]: #