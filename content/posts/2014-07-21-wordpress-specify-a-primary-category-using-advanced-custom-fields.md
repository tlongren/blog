---
title: 'WordPress Tip: Specify a Primary Category using Advanced Custom Fields'
author: Tyler Longren
type: post
date: 2014-07-21T12:49:19+00:00
url: /wordpress-specify-a-primary-category-using-advanced-custom-fields/
featured_image: /wp-content/uploads/2014/07/acf.png
primary_category:
  - WordPress
dsq_thread_id:
  - 2858278195
independent_publisher_primary_category:
  - WordPress
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cool
  - git
  - GitHub
  - Internet
  - Open Source
  - Personal
  - PHP
  - plugins
  - themes
  - WordPress
  - wordpress-plugins
  - wordpress-themes

---
## What WordPress custom fields should have been {.subtitle}

I found [Advanced Custom Fields][1] (also known as **ACF**) about 6 months ago while working on a project for a client. They didn&#8217;t want to have to mess around with editing the Custom Fields that come native with WordPress, it just wouldn&#8217;t have worked as smoothly.

The client needed to require one image, one PDF, one year selection, and one category. The category consisted of two options, &#8220;Weekly&#8221; or &#8220;Daily&#8221;. If you&#8217;re wondering, it was a newspaper client who wanted to categorize their posts as being either a &#8220;weekly issue&#8221; or a &#8220;daily issue&#8221;. Makes sense for a newspaper!

Getting the native WordPress custom fields to [play along well with files can be tricky][2], and probably not worth the effort, especially with a plugin like Advanced Custom Fields around.

So, enter the hero of this post, [Advanced Custom Fields][1]. I was able to set everything up with Advanced Custom Fields within about 20 minutes, and that even counts the time that I took to make various theme templates pull data from Advanced Custom Fields. The actual setup of Advanced Custom Fields took about 2 minutes.

I&#8217;ve since started using Advanced Custom Fields here at longren.io, too. [Independent Publisher][3], the WordPress theme I&#8217;ve been using, likes to show one main category when you&#8217;re viewing a single post, even if it&#8217;s not the most relevant category. So instead of a post about WordPress having the **Git** category shown at the top, I can now specify which category I want to be shown. So, for a post like this, I would obviously choose **WordPress** as my primary category.

I&#8217;ve already added the necessary parts to my Independent Publisher child theme, and have sent a pull request to [Raam Dev][4] to get his thoughts. It&#8217;s a very easy thing to support in a theme, however, it requires that everyone using that theme use the same field name in ACF.

I named my field **primary_category**, since that&#8217;s exactly what it is.  
<figure id="attachment_7155" aria-describedby="caption-attachment-7155" style="width: 578px" class="wp-caption aligncenter">[<img loading="lazy" src="https://i1.wp.com/longren.io/wp-content/uploads/2014/07/acf-field-setup-e1405853990377.png?resize=578%2C677" alt="Example field setup with Advanced Custom Fields" width="578" height="677" class="size-full wp-image-7155" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2014/07/acf-field-setup-e1405853990377.png?w=578&ssl=1 578w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/07/acf-field-setup-e1405853990377.png?resize=128%2C150&ssl=1 128w, https://i0.wp.com/www.longren.io/wp-content/uploads/2014/07/acf-field-setup-e1405853990377.png?resize=256%2C300&ssl=1 256w" sizes="(max-width: 578px) 100vw, 578px" data-recalc-dims="1" />][5]<figcaption id="caption-attachment-7155" class="wp-caption-text">Example field setup with Advanced Custom Fields</figcaption></figure>

After you&#8217;ve added your &#8220;Primary Category&#8221; custom field, you can then use the value of that field throughout your theme. I&#8217;ll have a short post later this week on exactly how you can display the primary category value in your theme. Or, if you want to know right now, you can [see this pull request at GitHub][6].

As you can tell, [Advanced Custom Fields][1] is a beast of a plugin. I also love that Advanced Custom Fields is totally free, which is kind of amazing to me. I&#8217;ve come across many paid plugins that are nowhere near as polished and user friendly as Advanced Custom Fields.

[Advanced Custom Fields][1] doesn&#8217;t skimp on the documentation, either. Their [documentation site][7] is extremely helpful, I never once ventured away from it while getting familiar with Advanced Custom Fields for the first time.

You can download Advanced Custom Fields [from the WordPress Plugin Directory][8], so you can also install it in just a few clicks, right from your WordPress Dashboard! Advanced Custom Fields is developed primarily by [Elliot Condon][9], and can [also be found on GitHub][10].

The great thing about this is that it can be applied to any theme, not just [Independent Publisher][3]. So, if you&#8217;re not using Independent Publisher, just setup Advanced Custom Fields as I described and make the necessary changes for your theme.

A follow-up post will have more details on using data from Advanced Custom Fields, no matter what theme you&#8217;re using. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7152"
					data-ulike-nonce="225d0de2fa"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7152"></button><span class="count-box"></span>
  </div>
</div>

[][11]{.later-button-el}

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

 [1]: http://www.advancedcustomfields.com/
 [2]: http://codex.wordpress.org/Using_Custom_Fields_to_attach_images,_links_or_files_to_a_post_easily
 [3]: https://github.com/raamdev/independent-publisher
 [4]: http://raamdev.com/
 [5]: https://i1.wp.com/longren.io/wp-content/uploads/2014/07/acf-field-setup-e1405853990377.png
 [6]: https://github.com/raamdev/independent-publisher/pull/122/files
 [7]: http://www.advancedcustomfields.com/resources/
 [8]: http://wordpress.org/plugins/advanced-custom-fields/
 [9]: http://www.elliotcondon.com/
 [10]: https://github.com/elliotcondon/acf
 [11]: #