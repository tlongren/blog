---
title: 'Circliful: A jQuery Plugin Providing Animated Progress Circles'
author: Tyler Longren
type: post
date: 2014-07-30T13:34:04+00:00
url: /circliful-a-jquery-plugin-providing-animated-progress-circles/
featured_image: /wp-content/uploads/2014/07/progress-circles.png
independent_publisher_primary_category:
  - JavaScript
dsq_thread_id:
  - 2896107858
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cool
  - css
  - git
  - GitHub
  - Internet
  - JavaScript
  - jquery
  - jquery plugin
  - Open Source
  - Personal
  - tools

---
 

## Animated progress circles

I use something similar, but not quite as nice (these are animated progress circles) on my [Work With Me][1] page. They don&#8217;t have percentages and are just hacked together from codepen.io.

The [jquery-plugin-circliful][2] repository on GitHub is way more advanced than what I have on my [Work With Me][1] page. Cicliful provides animated progress circles, which you [can see on the demo page][3].

[Circulful][2] is very easy to use. Just include jQuery and the Circliful JavaScript and CSS on your page:

<pre class="EnlighterJSRAW" data-enlighter-language="html" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">&lt;link href="css/jquery.circlify.css" rel="stylesheet" type="text/css" /&gt;

&lt;script src="http://code.jquery.com/jquery-1.10.2.min.js"&gt;&lt;/script&gt;
&lt;script src="js/jquery.circliful.min.js"&gt;&lt;/script&gt;</pre>

Add an element to your site with a unique ID:

<pre class="EnlighterJSRAW" data-enlighter-language="html" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">&lt;div id="myStat" data-dimension="250" data-text="35%" data-info="New Clients" data-width="30" data-fontsize="38" data-percent="35" data-fgcolor="#61a9dc" data-bgcolor="#eee" data-fill="#ddd" data-total="200" data-part="35" data-icon="long-arrow-up" data-icon-size="28" data-icon-color="#fff"&gt;&lt;/div&gt;
</pre>

Then, to get the progress circle to appear, add this JavaScript: 

<pre class="EnlighterJSRAW" data-enlighter-language="html" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">&lt;script&gt;
$( document ).ready(function() {
        $('#myStat').circliful();
    });
&lt;/script&gt;</pre>

There&#8217;s a **lot** of optional [_data-_ attributes][4] that you can set, as well. The entire list is below, straight from the [README][5].

  * dimension / is the height and width of the element / default is 200px on 200px
  * text / will be deisplayed inside of the circle over the info element
  * info / will be deisplayed inside of the circle bellow the text element (can be empty if you dont want to show info text)
  * width / is the size of circle / default is 15px
  * fontsize / is the font size for the text element / default is 15px
  * percent / can be 1 to 100
  * fgcolor / is the foreground color of the circle / default is #556b2f
  * bgcolor / is the background color of the cicle / default is #eee
  * fill / is the background color of the whole circle (can be empty if you dont want to set a background to the whole circle)
  * type / full or half circle for example data-type=&#8221;half&#8221; if not set the circle will be a full circle / default full circle
  * total / If you want to display the percentage of a value for example you have 750MB Ram and at the moment are 350MB in use. You need to set data-total=&#8221;750&#8243; and data-part=&#8221;350&#8243; and the circle will show the percentage value 36,85% 
  * part
  * border / Will change the styling of the circle. The line for showing the percentage value will be displayed inline or outline.
  * icon / Fontawesome icon class without the fa- before the class for example not fa-plus just plus
  * iconsize / Will set the font size of the icon.
  * iconcolor / Will set the font color of the icon.
  * animationstep / Will set the animation step, use 0 to disable animation, 0.5 to slow down, 2 to speed up, etc / default is 1

Circliful is [available on GitHub][2], there&#8217;s [also a demo][3]. I&#8217;ll eventually switch the progress circles on my Work With Me page to use [Circliful][2]. I mostly enjoy it&#8217;s ease of customization through _data-_ attributes.

If you need help configuring something, feel free to leave a comment. Make sure you look through [the issues that have already been reported][6], too.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7245"
					data-ulike-nonce="41bcf50657"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7245"></button><span class="count-box">1+</span>
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

 [1]: http://longren.io/work-with-me/
 [2]: https://github.com/pguso/jquery-plugin-circliful
 [3]: http://ladensia.com/circliful/
 [4]: https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_data_attributes
 [5]: https://github.com/pguso/jquery-plugin-circliful/blob/master/README.md
 [6]: https://github.com/pguso/jquery-plugin-circliful/issues
 [7]: #