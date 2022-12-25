---
title: Add Lightbox To All Images Embedded in a WordPress Post
author: Tyler Longren
type: post
date: 2014-03-01T20:35:35+00:00
url: /add-rellightbox-to-all-images-embedded-in-a-wordpress-post/
featured_image: /wp-content/uploads/2014/03/lightbox1.png
dsq_thread_id:
  - 2325990849
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
independent_publisher_primary_category:
  - WordPress
tags:
  - how-to
  - Internet
  - Personal
  - php tutorials
  - theme
  - themes
  - WordPress
  - wordpress-themes

---
 

## Make every image in a post open in a lightbox

I needed to do this about a year ago, attach `rel="lightbox"` to every image inside a WordPress post, so that the image would open in a lightbox. The lightbox plugin we were using wasn&#8217;t adding rel=&#8221;lightbox&#8221; to some images for whatever reason, so this was my quick alternative. Turned out to be incredibly simple with WordPress&#8217;s `add_filter()` function.

`add_filter()` allows developers to hook a function up to a specific **filter action**. There&#8217;s [TONS of action and filter hooks available][1], some are really, really useful. A great introduction to filter and actions hooks can be found at [WPCandy][2] or [in the WordPress Codex][3]. Smashing WordPress [has a quite detailed article, too][4].

Anyway, as usual, when adding this type of thing to WordPress, drop this code in your theme&#8217;s functions.php file to get this working:

<pre class="wp-block-preformatted">function add_lightbox_rel($content) {
       global $post;
       $pattern ="/&lt;a(.*?)href=('|")(.*?).(bmp|gif|jpeg|jpg|png)('|")(.*?)>/i";
       $replacement = '&lt;a$1href=$2$3.$4$5 rel="lightbox" title="'.$post->post_title.'"$6>';
       $content = preg_replace($pattern, $replacement, $content);
       return $content;
}
add_filter('the_content', 'add_lightbox_rel');</pre>

**You should be aware** that some plugins don&#8217;t use `rel="lightbox"` for activating their lightbox/colorbox overlay. So, if that&#8217;s the case, just modify the `theme_add_lightbox_rel()` function and change `rel="lightbox"` to `rel="whatever-plugin-uses"` in the `$replacement` variable (on line 5).

That&#8217;s it! Save your functions.php file and you should have lightboxes on all the images embedded in your post!

### Plugin Alternative

If you&#8217;d prefer to achieve this with a plugin, I&#8217;d suggest [jQuery Colorbox][5]. It does a really nice job of grouping gallery images, used for the next and previous links for navigating the gallery images.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5476"
					data-ulike-nonce="7dddc2a8cc"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5476"></button><span class="count-box">2+</span>
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

 [1]: http://adambrown.info/p/wp_hooks/hook
 [2]: http://wpcandy.com/teaches/how-to-use-wordpress-hooks/
 [3]: http://codex.wordpress.org/Plugin_API/Action_Reference
 [4]: http://wp.smashingmagazine.com/2012/02/16/inside-wordpress-actions-filters/
 [5]: http://wordpress.org/plugins/jquery-colorbox/
 [6]: #