---
title: Jerome’s Keywords and WordPress 2.0
author: Tyler Longren
type: post
date: 2005-12-03T05:24:29+00:00
url: /jeromes-keywords-and-wordpress-20/
views:
  - 3323
ratings_users:
  - 1
ratings_score:
  - 5
ratings_average:
  - 5
dsq_thread_id:
  - 1385916442
tags:
  - blog
  - blogs
  - Jeromes-Keywords
  - keywords
  - news
  - PHP
  - plugins
  - software
  - tags
  - WordPress
  - wordpress-2
  - wordpress-2-0
  - wordpress-2.0

---
I was having [some problems][1] with my keywords getting deleted when updating a post (using [Jerome&#8217;s Keywords 1.8][2]). The problem was a result of a blank textarea on the page to edit a post. Wasn&#8217;t hard to fix at all.

The textarea, with a header of &#8220;Keywords&#8221;, shows up blank when editing a post. The initial post is good because that text area is filled out manually. jeromes-keywords.php was using &#8220;$postdata->ID&#8221; as a reference in the get\_post\_meta() function. $postdata->ID didn&#8217;t contain any value at all.

After doing a little digging, I found I could get a posts ID using $post->ID, notice the missing &#8220;data&#8221;. It only takes a few steps to get [Jerome&#8217;s Keywords][2] working 100% in WordPress 2.0.  
**1.** Open wp-content/plugins/jeromes-keywords.php in a text editor.  
**2.** On line 553, change the line that says &#8220;global $postdata, $content&#8221; to read &#8220;global $post, $content&#8221;.  
**3.** On line 555, change &#8220;get\_post\_meta($postdata->ID, KEYWORDS\_META, true)&#8221; to &#8220;get\_post\_meta($post->ID, KEYWORDS\_META, true)&#8221;.  
**4.** Save jeromes-keywords.php, you&#8217;re done.

After doing that, the keywords textarea created by the plugin will be populated with your original keywords. I guess that textarea must have the keywords there all the time, even when editing. Before, my keywords weren&#8217;t in the &#8220;keywords&#8221; textarea, they were only in a custom field.  
<!--adsense-->

  
It appears that [Jerome&#8217;s Keywords][2] deletes post meta every time that post is edited. And I think that&#8217;s the desired functionality for some reason. I only say that after looking at the code for a half hour or so. I think the post would end up with one custom field named &#8220;keywords&#8221; for every time the post is edited or updated. So, update a post 4 times and you&#8217;ll have 4 identical custom fields named &#8220;keywords&#8221;.

All of my favorite plugins are now working very well for me with [WordPress 2.0-RC1][1].  
<!--adsense#googlePackRefer-->

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2109"
					data-ulike-nonce="90f7d73455"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2109"></button><span class="count-box"></span>
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

 [1]: http://www.longren.org/archives/2104
 [2]: http://vapourtrails.ca/wp-keywords
 [3]: #