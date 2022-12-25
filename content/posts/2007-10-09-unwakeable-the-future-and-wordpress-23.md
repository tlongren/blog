---
title: 'Unwakeable: The Future And WordPress 2.3'
author: Tyler Longren
type: post
date: 2007-10-10T02:39:41+00:00
url: /unwakeable-the-future-and-wordpress-23/
ratings_users:
  - 7
ratings_score:
  - 10
ratings_average:
  - 5
views:
  - 3073
dsq_thread_id:
  - 1385906870
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - Internet
  - JavaScript
  - k2
  - Noteworthy
  - Personal
  - PHP
  - Unwakeable
  - WordPress
  - wordpress-theme

---
I&#8217;ve waited far too long to post an update on [Unwakeable][1] 2.0 and it&#8217;s status, so here it is, almost. First, I&#8217;d like to address the issues with the current Unwakeable release (version 1.2.1) and WordPress 2.3. There&#8217;s a few issues, although most of them are fairly minor.  
<!--adsense-->

  
**1. Tags:** Unwakeable 1.2.1 does not support the new tagging system in WordPress 2.3. If you&#8217;re using the new tagging system, your tags will not be displayed. Ultimate Tag Warrior still works just fine with Unwakeable 1.2.1 and WordPress 2.3.

**2. Prototype:** Livesearch (and probably rolling archives) don&#8217;t work with WordPress 2.3. I really have no idea why, it&#8217;s probably a combination of a few things. One major contributor is probably the fact that WordPress 2.3 likes jQuery instead of Prototype, and Unwakeable relies heavily on Prototype for it&#8217;s ajax effects, such as livesearch, rolling archives, and live commenting. I only use livesearch, so I can&#8217;t say for certain if rolling archives and live commenting were truly broken. All I know is Firefox CPU usage skyrockets when loading this site when livesearch is enabled.

**3. Archives Page:** The archives page is slightly broken, it displays an error similar to this at the top:

> WordPress database error: [Table &#8216;tlongren\_wordpress.wp\_categories&#8217; doesn&#8217;t exist]

That happens because Unwakeable 1.2.1 doesn&#8217;t know about [the new taxonomy schema in WordPress 2.3][2]. WordPress 2.3 does away with three tables, categories, post2cat, and link2cat. Those tables are replaced by three new tables that, when combined, offer much greater flexibility in handling post categories and blogroll categories. I think this new schema handles tags as well.

**4.Tag Archives:** This may be unique to this site, I haven&#8217;t tested, but whenever you try to visit a tag archive (my [unwakeable tag archive][3] for example), a 404 is received. Obviously, it should display all the posts with the given tag. Can anyone using Unwakeable 1.2.x confirm this is also broken on their WordPress 2.3 site?

**5. Unknowns:** There&#8217;s probably lots of broken things I&#8217;m not aware of. K2 Sidebar Modules may very well be one of them. I really doubt they work 100% because they make some use of categories. If you&#8217;ve got anything I&#8217;ve missed, please let me know about it so I can make sure it&#8217;s working in Unwakeable 2.0. One thing that DOES work that I entirely expected to be broken are the category archives. I was ready for all sorts of errors when trying to view a category archive, like the [Unwakeable category archive][4], but they display exactly as they did with WordPress 2.2.x. Please let me know if you&#8217;re aware of any other incompatibilities between Unwakeable 1.2.x and WordPress 2.3.  
<!--more-->

  
<!--adsense-->

  
Now that all that ugly broken stuff is behind us, let&#8217;s move on to Unwakeable 2.0 and where it sits currently and where it&#8217;s headed. This will probably take a while, so get comfortable. Anyway, about a month ago, I was days away from releasing Unwakeable 2.0 to the public. I had everything exactly as I wanted it and realized it would not work entirely with [WordPress][5] 2.3, as I explained above. WordPress 2.3 was still a couple months from being released at that time.

At that point, I stopped everything and took a fair amount of time to think the situation over. I even contemplated abandoning Unwakeable altogether, mostly due to my lack of free time. Anyway, I basically had two options (aside from ceasing development of Unwakeable), either fix the current Unwakeable code or re-build Unwakeable 2.0 from a more recent revision of [K2][6]. I knew the latest revisions of [K2][6] were mostly (if not fully) compatible with WordPress 2.3.

I immediately upgraded this site to WordPress 2.3 upon it&#8217;s official release only to find that livesearch (and probably rolling archives) were horribly broken, as I described before. Luckily, K2 has been [using jQuery since revision 382][7], Prototype is no longer required by K2. After I realized K2 was now making use of jQuery, I knew the best option for me would be to base Unwakeable 2.0 off a newer version of K2. That leads right to the current reason Unwakeable 2.0 has yet to be released, and that&#8217;s the current status of K2.

K2 release candidate 3 [dropped earlier today][8], almost exactly a week after [release candidate 2 became available][9]. I&#8217;ve noticed a significant increase in the number of commits to K2 svn in the last month or so, indicating lots of work being done on K2. Because of this, I&#8217;m waiting for the final stable release of K2 to use as a starting point for Unwakeable 2.0. I should be able to release Unwakeable 2.0 in a matter of days following the stable release of K2.

I think Unwakeable 2.0 will be one of the most robust WordPress themes around once it&#8217;s released. K2 alone sports some great features, Unwakeable 2.0 will add to that feature-set. The combination of features should make Unwakeable irresistible to many bloggers.

Unwakeable 2.0 includes a number of style related options that can be set right from the options page. These will let you set various colors Unwakeable should use in the header and menu. The list of customizable style settings will only grow in future versions Unwakeable, assuming I get enough suggestions from Unwakeable users. I&#8217;m starting out with a fairly basic set of colors and options to configure, mostly items in the header such as the menu color and the menu color when the mouse cursor is hovering over it.

You can see the items that can be customized/styled in the image below, just click the thumbnail for the full size image. That screenshot was taken from my most recent test version of Unwakeable 2.0, still based off of the old K2. The final 2.0 release will be roughly the same. Have a look below:

<a href="https://i2.wp.com/www.longren.org/images/unwakeable_2.0_starteroptions.png" rel="thumbnail" title="Unwakeable 2.0 Customization Options"><img src="https://i1.wp.com/www.longren.org/images/unwakeable_2.0_starteroptions-thumb.jpg?w=1100" alt="Unwakeable 2.0 Customization Options" align="left" data-recalc-dims="1" /></a>I&#8217;d like to hear from actual Unwakeable users on what they&#8217;d like to be able to customize, I know lots of you go to great lengths to customize Unwakeable. My ultimate goal with Unwakeable is to give you, the user, the ability to style and customize as much as you want/need to right from the options page. Storing styling options in the WordPress database will save your styling settings when upgrading to new versions of Unwakeable. This will prevent the need to edit PHP code or modify the CSS code to get the color scheme and overall style desired.

Now, you may be asking yourself, &#8220;What&#8217;s the point when custom style sheets can be used?&#8221;. Custom style sheets, or schemas as they&#8217;re called in K2 and Unwakeable, allow users to create a CSS file to modify their blogs appearance. Styles are intended to allow you to keep the same color scheme and general style across many versions of K2 or Unwakeable, without the need to modify any of the CSS. You&#8217;d simply tell K2 or Unwakeable to use your custom style sheet, no matter what the theme version, to get your desired color scheme. This is a good solution for maintaining the same style when upgrading to a new version of K2 or Unwakeable. It prevents you from having to edit the themes core files, which may change from version to version. However, there&#8217;s a usability problem with using custom style sheets to maintain the same style. The problem is, many users do not know enough CSS to get the look they want, either that or they don&#8217;t care to spend the time creating a custom style sheet.

Unwakeable will give you an extremely easy to use, straight-forward interface for manipulating your blogs appearance. I am going to focus heavily on adding customizable style settings to the options page throughout the 2.x versions of Unwakeable. If you use a custom style sheet, fear not, K2 styles should still work in Unwakeable 2.0. Those of you currently using a custom style sheet should probably stick with the custom style sheet, it will give you much greater flexibility than the fairly simple options Unwakeable provides an interface for. It&#8217;d be impossible for me to add options that allow you to style every single piece of Unwakeable that can be taken care of with a custom style sheet.

So, all you Unwakeable users out there, please leave comments at this post or on [the official Unwakeable page][1] with what you&#8217;d like to be able to style or customize. It can be anything from customizing colors in a certain area of Unwakeable to choosing fonts to use for post titles or post content.

I can&#8217;t guarantee I&#8217;ll add your request to Unwakeable 2.0, but if I think others will benefit from it, I will do my best to get it into Unwakeable 2.0. I may push Unwakeable 2.0 out with it&#8217;s current feature set as soon as I&#8217;ve got everything built into a stable K2 version. If I do that, I&#8217;ll work on adding your requests to version 2.1, which shouldn&#8217;t be all that far behind the release of 2.0. If that ends up being the case, I&#8217;d suggest everyone who makes lots of style mods wait for 2.1 to come out, so all (hopefully) of your customizations will be saved, making future upgrades a breeze.  
<!--adsense-->

  
There&#8217;s a few other features that you&#8217;ll notice in Unwakeable 2.0, some of which [I discussed in this post in August][10]. One feature I think a lot of users will really appreciate is the option to use flexible page widths. Flexible page width can only be used when one sidebar is in use. If you&#8217;ve got two sidebars, the width basically takes up the entire width of the browser window, so two sidebars with flexible page width enabled would make the page wider than the browser window, causing visitors to have to scroll horizontally on your site to see some things on either sidebar. That may not be the case for people running @ super high screen resolutions, but when I run at 1600&#215;1200, there&#8217;s barely enough room to fit everything on the screen without a horizontal scroll bar appearing.

One final thing, would anyone like to volunteer to test Unwakeable 2.0 in the near future? Things often work perfectly for me but seem to break under different environments. If nobody wants to volunteer, I&#8217;ll probably just release a public beta or something after I&#8217;ve got all the current features moved over to a stable K2 release.

As always, questions, comments, and constructive criticism are welcome and appreciated. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2333"
					data-ulike-nonce="2ef54f2327"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2333"></button><span class="count-box"></span>
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

 [1]: http://www.longren.org/wordpress/unwakeable/
 [2]: http://boren.nu/archives/2007/08/26/wordpress-23-taxonomy-schema/
 [3]: http://www.longren.org/tag/unwakeable/
 [4]: http://www.longren.org/category/internet/wordpress/unwakeable/
 [5]: http://www.wordpress.org/
 [6]: http://www.getk2.com/
 [7]: http://getk2.com/2007/08/k2-and-jquery-sitting-a-tree/
 [8]: http://getk2.com/2007/10/k2-release-candidate-3-released/
 [9]: http://getk2.com/2007/10/k2-release-candidate-2/
 [10]: http://www.longren.org/2007/08/02/unwakeable-and-vacation/
 [11]: #