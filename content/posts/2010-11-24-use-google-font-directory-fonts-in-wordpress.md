---
title: Use Google Font Directory Fonts in WordPress
author: Tyler Longren
type: post
date: 2010-11-25T03:46:33+00:00
url: /use-google-font-directory-fonts-in-wordpress/
ratings_users:
  - 3
ratings_score:
  - 15
ratings_average:
  - 5
views:
  - 248
dsq_thread_id:
  - 1385912691
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - code
  - css
  - google
  - Internet
  - Noteworthy
  - Personal
  - WordPress

---
Google has some seriously nice looking fonts available for you to use for free in the [Google Font Directory][1]. All the fonts are under an open source license and are served right from Google servers.

Most modern web browsers [support webfonts][2]. The [Google Font API FAQ][3] would be a good place to visit if you have questions or are curious about some of the limitations.

Making use of these fonts in your WordPress theme is extremely easy, as long as you have a basic understanding of [CSS][4]. Now let&#8217;s get down to using these in your WordPress theme, we&#8217;ll keep it short and simple.

First, head over to the [Google Font Directory][5] and pick a font to use. I&#8217;ll be using [IM Fell][6] as an example, since that&#8217;s the font I use for post titles on this site.

Once you find a font you like, click on it. If the font you chose has variants, you will need to click on a variant to use. Once you&#8217;re on the font page, click the &#8220;Get the code&#8221; tab and google will generate the code for the font. You will embed this code in the **header.php** file for your theme. I usually put it right before the line that calls the theme stylesheet file. Here&#8217;s the code I used to include the IM Fell font:

<pre>&lt;link href='http://fonts.googleapis.com/css?family=IM+Fell+DW+Pica&subset=latin' rel='stylesheet' type='text/css' /&gt;</pre>

After that, all you have to do is use the font in your CSS, typically the **style.css** file in your WordPress theme directory. To get my post titles to use the IM Fell font, I did this:

<pre>.entry-title, h3 {
    font-family: 'IM Fell DW Pica', arial, serif;
    font-size: 28px;
    font-weight: 600;
}
</pre>

The **font-size** property defines what size of font to use (duh!). The **font-weight** property defines the thickness of the font (degree of boldness). You can apply the font-family property using the Google Font to pretty much any piece of CSS that targets text. You can use it for post content, links, widget titles, or whatever you want really.

If you have any questions, feel free to leave a comment and I&#8217;ll do my best to help you out! 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2630"
					data-ulike-nonce="5472c20e39"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2630"></button><span class="count-box"></span>
  </div>
</div>

[][7]{.later-button-el}

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

 [1]: https://fonts.google.com/
 [2]: http://code.google.com/apis/webfonts/faq.html#Browsers_Supported
 [3]: http://code.google.com/apis/webfonts/faq.html
 [4]: http://www.w3schools.com/css/
 [5]: http://code.google.com/webfonts/
 [6]: http://code.google.com/webfonts/list?family=IM+Fell&subset=latin
 [7]: #