---
title: Install All Google Web Fonts on Ubuntu, Easily
author: Tyler Longren
type: post
date: 2014-01-16T02:52:30+00:00
url: /install-all-google-web-fonts-on-ubuntu-easily/
featured_image: /wp-content/uploads/2014/01/typecatcher.png
dsq_thread_id:
  - 2127996748
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
independent_publisher_primary_category:
  - Linux
tags:
  - cool
  - Internet
  - Linux
  - Open Source
  - Personal
  - ubuntu
  - xubuntu

---
 

There&#8217;s a few different ways to install the Google Web fonts on your Ubuntu system. [Web UPD8 provides a script][1] that does it for you.

Another way is to use TypeCatcher, as [suggested by Jack Wallen at TechRepublic][2]. You can install TypeCatcher via a PPA, which means easy updates. No auto-updates with the script method, unfortunately.

To install TypeCatcher via PPA, open a terminal and run `sudo add-apt-repository ppa:andrewsomething/typecatcher` and then run `sudo apt-get update && sudo apt-get install typecatcher`. That&#8217;s it, TypeCatcher should show up in your applications menu. If you&#8217;re using Xubuntu, it&#8217;s under Accessories.

I&#8217;d never heard of [TypeCatcher][3] until I came across Jack&#8217;s post at TechRepublic. Installed it on Xubuntu 13.10 and fell in love with it. Just select a font, and click the install button, done. The featured image for this post is TypeCatcher with the Lato font selected. For more details on TypeCatcher, [go read Jack&#8217;s post][2].

If you can&#8217;t use a PPA, or don&#8217;t want to, you&#8217;ve still got a good option for easily installing the fonts with the script from Web UPD8. If you&#8217;d like to see how the script works, you can find it below or [download it here][4]. It essentially just using [Mercurial][5] to install them.

<pre class="EnlighterJSRAW" data-enlighter-language="shell" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group=""># Original author: Michalis Georgiou &lt;mechmg93@gmail.comr>
# Modified by Andrew http://www.webupd8.org &lt;andrew@webupd8.org>

_wgeturl="https://github.com/google/fonts/archive/master.tar.gz"
_gf="google-fonts"

# install wget
sudo apt-get install wget

# make sure a file with the same name doesn't already exist
rm -f $_gf.tar.gz

echo "Connecting to Github server..."
wget $_wgeturl -O $_gf.tar.gz

echo "Extracting the downloaded archive..."
tar -xf $_gf.tar.gz

echo "Creating the /usr/share/fonts/truetype/$_gf folder"
sudo mkdir -p /usr/share/fonts/truetype/$_gf

echo "Installing all .ttf fonts in /usr/share/fonts/truetype/$_gf"
find $PWD/fonts-master/ -name "*.ttf" -exec sudo install -m644 {} /usr/share/fonts/truetype/google-fonts/ ; || return 1

echo "Updating the font cache"
fc-cache -f > /dev/null

# clean up, but only the .tar.gz, the user may need the folder
rm -f $_gf.tar.gz

echo "Done."</pre>

For instructions on how to install the script from Web UPD8, head over to their [post about it][1], everything you need [will be there][1]. See? I just linked it twice for ya.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="5084"
					data-ulike-nonce="1b663e8adc"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_5084"></button><span class="count-box"></span>
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

 [1]: http://www.webupd8.org/2011/01/automatically-install-all-google-web.html
 [2]: http://www.techrepublic.com/blog/linux-and-open-source/easily-install-google-web-fonts-in-ubuntu-with-typecatcher/
 [3]: http://andrewsomething.wordpress.com/2012/11/11/introducing-typecatcher/
 [4]: http://webupd8.googlecode.com/files/install-google-fonts
 [5]: http://mercurial.selenic.com/
 [6]: #