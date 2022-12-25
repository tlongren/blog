---
title: 'RemindToRead: Email Users a Reminder to Finish Reading Your Articles'
author: Tyler Longren
type: post
date: 2015-08-24T12:00:44+00:00
url: /remindtoread-email-users-a-reminder-to-finish-reading-your-articles/
featured_image: /wp-content/uploads/2015/08/remind-to-read-front-page-2.png
independent_publisher_primary_category:
  - Services, Tools
dsq_thread_id:
  - 4043898995
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cool
  - GitHub
  - Internet
  - services
  - tools
  - WordPress

---
## Provide your users a world-class post-visit experience {.subtitle}

I liked the idea of using [RemindToRead.com][1] on this site when I [saw it on Hacker News][2] the other day. I got in touch with [Leonard Bogdonoff][3] and expressed interest. He, in turn, offered to let me test it out here at longren.io.

Leonard setup some JS for my site for a quick test and gave me all the necessary code in a shared Google Doc. Took all of 5 minutes to get setup.

You can see it in action at the end of every post here at longren.io. It appears at the very end of every post, but only when viewing an [individual post][4]. The button looks like this:  
[<img loading="lazy" src="https://i2.wp.com/longren.io/wp-content/uploads/2015/08/remind-to-read-button.png?resize=163%2C53" alt="remind-to-read-button" width="163" height="53" class="aligncenter size-full wp-image-8124" srcset="https://i1.wp.com/www.longren.io/wp-content/uploads/2015/08/remind-to-read-button.png?w=163&ssl=1 163w, https://i1.wp.com/www.longren.io/wp-content/uploads/2015/08/remind-to-read-button.png?resize=150%2C49&ssl=1 150w" sizes="(max-width: 163px) 100vw, 163px" data-recalc-dims="1" />][5]

### Is RemindToRead Ready For Production?

Getting closer, just from the changes I saw on the dashboard today and the very straight-forward registration process. Signup requires minimal effort. Just enter your email, [choose a password][6], receive an email containing a confirmation link, click the confirmation link, update password, and continue on with setup. A temporary email sent after user signup can be seen below.  
[<img loading="lazy" src="https://i0.wp.com/longren.io/wp-content/uploads/2015/08/remind-to-read-welcome-email-temporary-1024x596.png?resize=700%2C407" alt="remind-to-read-welcome-email-temporary" width="700" height="407" class="aligncenter size-large wp-image-8111" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2015/08/remind-to-read-welcome-email-temporary.png?resize=1024%2C596&ssl=1 1024w, https://i0.wp.com/www.longren.io/wp-content/uploads/2015/08/remind-to-read-welcome-email-temporary.png?resize=150%2C87&ssl=1 150w, https://i0.wp.com/www.longren.io/wp-content/uploads/2015/08/remind-to-read-welcome-email-temporary.png?resize=300%2C175&ssl=1 300w, https://i0.wp.com/www.longren.io/wp-content/uploads/2015/08/remind-to-read-welcome-email-temporary.png?resize=700%2C407&ssl=1 700w, https://i0.wp.com/www.longren.io/wp-content/uploads/2015/08/remind-to-read-welcome-email-temporary.png?w=1334&ssl=1 1334w" sizes="(max-width: 700px) 100vw, 700px" data-recalc-dims="1" />][7]

The current iteration of the dashboard is not quite finished, but is very functional as it stands, even it&#8217;s early stages. It provides easy to follow instructions for adding RemindToRead code to your website. Just include some JavaScript and add this little snippet where you want the RemindToRead button to show:

<pre class="lang:xhtml decode:true " >&lt;a href="#" class="later-button-el"&gt;&lt;/a&gt;</pre>

Here&#8217;s what the dashboard currently looks like:  
[<img loading="lazy" src="https://i0.wp.com/longren.io/wp-content/uploads/2015/08/remindtoread-dash-1024x425.png?resize=700%2C291" alt="remindtoread-dash" width="700" height="291" class="aligncenter size-large wp-image-8136" srcset="https://i2.wp.com/www.longren.io/wp-content/uploads/2015/08/remindtoread-dash.png?resize=1024%2C425&ssl=1 1024w, https://i2.wp.com/www.longren.io/wp-content/uploads/2015/08/remindtoread-dash.png?resize=150%2C62&ssl=1 150w, https://i2.wp.com/www.longren.io/wp-content/uploads/2015/08/remindtoread-dash.png?resize=300%2C125&ssl=1 300w, https://i2.wp.com/www.longren.io/wp-content/uploads/2015/08/remindtoread-dash.png?resize=700%2C291&ssl=1 700w, https://i2.wp.com/www.longren.io/wp-content/uploads/2015/08/remindtoread-dash.png?w=1891&ssl=1 1891w" sizes="(max-width: 700px) 100vw, 700px" data-recalc-dims="1" />][8]

I simply added the code above to my relevant template file so that it&#8217;s displayed at the end of every post, but is only shown when viewing a single post. So you won&#8217;t see the button on archive pages, tags pages, category pages, search results, etc.

### A WordPress Plugin Coming

A [GitHub repo already exists for a WordPress plugin][9], I&#8217;ve not tried it out yet, but plan to later today and will report back. I know there&#8217;s been a lot of core changes to RemindToRead recently, the WordPress plugin may have some catching up to do.

The plugin looks pretty solid code-wise, after a real quick glance. Sounds like Leonard may want me to maintain the WordPress plugin, should be a piece of cake once the core of everything starts to take its final shape. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="8106"
					data-ulike-nonce="7e9e95c8a6"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_8106"></button><span class="count-box">8+</span>
  </div>
</div>

[][10]{.later-button-el}

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

 [1]: https://remindtoread.com/
 [2]: https://news.ycombinator.com/item?id=10048798
 [3]: http://www.rememberlenny.com/
 [4]: https://longren.io/using-remindtoread/
 [5]: https://i2.wp.com/longren.io/wp-content/uploads/2015/08/remind-to-read-button.png
 [6]: https://passwds.io/
 [7]: https://i0.wp.com/longren.io/wp-content/uploads/2015/08/remind-to-read-welcome-email-temporary.png?ssl=1
 [8]: https://i1.wp.com/longren.io/wp-content/uploads/2015/08/remindtoread-dash.png?ssl=1
 [9]: https://github.com/RemindToRead/remindtoread-wordpress
 [10]: #