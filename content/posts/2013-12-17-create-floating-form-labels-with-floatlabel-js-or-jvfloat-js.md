---
title: Create Floating Form Labels with FloatLabel.js or JVFloat.js
author: Tyler Longren
type: post
date: 2013-12-18T04:22:01+00:00
url: /create-floating-form-labels-with-floatlabel-js-or-jvfloat-js/
featured_image: /wp-content/uploads/2013/12/float.png
dsq_thread_id:
  - 2057680071
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cool
  - GitHub
  - Internet
  - JavaScript
  - jquery
  - kegplan.io
  - Open Source
  - Personal
  - zepto

---
Floating labels are cool. People tend to have pretty strong opinions about floating labels, but overall, I like the idea, and have liked most implementations I&#8217;ve seen. The first one I saw [was on CodePen][1]. There&#8217;s [a good article @mds][2] on how the design pattern got started. There&#8217;s a lot of other cool thoughts on floating labels, specifically how they enhance (or undermine) the end user&#8217;s experience.

## Where It Started

The Floating Labels pattern was based on a [concept by Matt D. Smith][3]. You can read more about the history of the floating label pattern [at this blog post][4].  
[<img loading="lazy" src="https://i1.wp.com/www.longren.org/images/float_pattern.gif?resize=600%2C400" alt="Original from Matt D. Smith" width="600" height="400" class="aligncenter size-full wp-image-11111111111111" data-recalc-dims="1" />][5]  
A [search for &#8220;floating labels&#8221; on CodePen][6] return about 200 results. You could probably take code from any of those pens and use it to implement a possibly slimmer floating label pattern for yourself. But, how can you choose which is the best way to do floating labels?

## I Like Plugins

Personally, I like to roll with jQuery plugins for this sort of thing. The smaller the plugin, the better.  
[<img loading="lazy" src="https://i1.wp.com/longren.io/wp-content/uploads/2013/12/jvfloat.png?resize=603%2C159&#038;ssl=1" alt="jvfloat" width="603" height="159" class="aligncenter size-full wp-image-4984" srcset="https://i1.wp.com/www.longren.io/wp-content/uploads/2013/12/jvfloat.png?w=603&ssl=1 603w, https://i1.wp.com/www.longren.io/wp-content/uploads/2013/12/jvfloat.png?resize=300%2C79&ssl=1 300w" sizes="(max-width: 603px) 100vw, 603px" data-recalc-dims="1" />][7]  
I&#8217;ve used [JVFloat][8] and really like it. Super easy to implement and the styling is extremely minimal by default, which is a good thing. The default looks decent with pretty much any UI but can easily be modified via CSS.

[FloatLabel.js][9] is similar to JVFloat. The CSS that comes with FloatLabel.js is also extremely minimal and can be easily customized to fit your UI. I am going to be using FLoatLabel.js in future projects, like [kegplan.io][10].

## Responsive Ready?

FloatLabel.js appears to have better responsive support. In JVFloat, the floated labels and their respective input fields are really scrunched together, in the default CSS at least.  
[<img loading="lazy" src="https://i0.wp.com/longren.io/wp-content/uploads/2013/12/Screenshot-12172013-055950-PM-242x300.png?resize=242%2C300&#038;ssl=1" alt="FloatLabel.js" width="242" height="300" class="alignright size-medium wp-image-4980" srcset="https://i0.wp.com/www.longren.io/wp-content/uploads/2013/12/Screenshot-12172013-055950-PM.png?resize=242%2C300&ssl=1 242w, https://i0.wp.com/www.longren.io/wp-content/uploads/2013/12/Screenshot-12172013-055950-PM.png?w=398&ssl=1 398w" sizes="(max-width: 242px) 100vw, 242px" data-recalc-dims="1" />][11]I haven&#8217;t witnessed this problem with FloatLabel.js. [Check out the FloatLabel.js demo][12] to see how it responds when you resize your browser window. Now have a look at the JVFloat demo, and again, resize your browser window to see how it responds. JVFloat.js doesn&#8217;t look as good as FloatLabel.js, it&#8217;s that simple.

So, if you&#8217;re looking for a good floating labels plugin I&#8217;d suggest [FloatLabel.js][9], as it&#8217;s more responsive-friendly than [JVFloat][8]. Both are great jQuery plugins, though. And one bonus is that JVFloat is also a [Zepto][13] plugin.

## Installation, finally!

Both are extremely easy to implement on your site. Just include the js and css like you usually would. But here&#8217;s more detail.

### JVFloat.js

  1. Upload CSS and JS files.
  2. Add <span class="lang:default decode:true  crayon-inline " ><link rel=&#8221;stylesheet&#8221; href=&#8221;css/jvfloat.css&#8221;></span> to your <span class="lang:default decode:true  crayon-inline " ><head></span> section.
  3. Add <span class="lang:default decode:true  crayon-inline " ><script src=&#8221;js/jvfloat.min.js&#8221;></script></span> right before the closing <span class="lang:default decode:true  crayon-inline " ></body></span> tag. Be sure you&#8217;ve loaded jQuery (or Zepto) first.
  4. Initialize JVFloat somewhere in your javascript (or on page directly in script tags) <span class="lang:default decode:true  crayon-inline " >$(&#8216;.float&#8217;).jvFloat();</span> 
  5. Add <span class="lang:default decode:true  crayon-inline " >class=&#8221;float&#8221;</span> to text input fields you wish to have floating labels.

### FloatLabel.js

FloatingLabels.js is probably quite similar. Since I&#8217;ve never used it, I won&#8217;t give you step-by-step directions since I have no experience with it (yet). Instead, refer to the [README file][14] at the [FLoatLabel.js GitHub repo][15]. It has installation instructions, I just haven&#8217;t tested them quite yet.

I really suggest you [read this post from Brad Frost][16] before voting. He gives some very good, specific examples of pros and cons of floating labels.  


<div id="polls-13" class="wp-polls">
</div>

<div id="polls-13-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

Comments are open below or you can [discuss on Hacker News][17].

**Update December 30, 2013:** Also, check out [Label Better][18], by Pete R. It looks really nice and easy to setup and integrate. You can find [a demo over here][19]. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="4971"
					data-ulike-nonce="df5d9ae3fb"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_4971"></button><span class="count-box"></span>
  </div>
</div>

[][20]{.later-button-el}

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

 [1]: http://codepen.io/aaronbarker/pen/tIprm
 [2]: http://mattdsmith.com/float-label-pattern/
 [3]: http://dribbble.com/shots/1254439--GIF-Mobile-Form-Interaction?list=users
 [4]: http://blog.mahardi.me/2013/10/14/jvfloatjs---the-experiment-with-form-accessbility-and-ux-in-html5/
 [5]: https://i1.wp.com/www.longren.org/images/float_pattern.gif
 [6]: http://codepen.io/search?q=floating+label&limit=all&depth=everything
 [7]: https://i2.wp.com/www.longren.org/wp-content/uploads/2013/12/jvfloat.png
 [8]: https://github.com/maman/JVFloat.js
 [9]: https://github.com/m10l/FloatLabel.js
 [10]: http://kegplan.io/
 [11]: https://i2.wp.com/www.longren.org/wp-content/uploads/2013/12/Screenshot-12172013-055950-PM.png
 [12]: http://labs.mikemitchell.co.uk/FloatLabelJS/
 [13]: http://zeptojs.com/
 [14]: https://github.com/m10l/FloatLabel.js/blob/master/README.md
 [15]: https://github.com/m10l/FloatLabel.js/blob/master/
 [16]: http://bradfrostweb.com/blog/post/float-label-pattern/
 [17]: https://news.ycombinator.com/item?id=6925895
 [18]: https://github.com/peachananr/label_better
 [19]: http://www.thepetedesign.com/demos/label_better_demo.html
 [20]: #