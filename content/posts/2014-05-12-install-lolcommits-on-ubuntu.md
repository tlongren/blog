---
title: 'How-To: Install lolcommits On Ubuntu'
author: Tyler Longren
type: post
date: 2014-05-12T12:36:27+00:00
url: /install-lolcommits-on-ubuntu/
featured_image: /wp-content/uploads/2014/05/lolcommits.jpg
dsq_thread_id:
  - 2678506644
primary_category:
  - Cool
independent_publisher_primary_category:
  - Linux
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cool
  - Funny
  - git
  - GitHub
  - how-to
  - howto
  - Internet
  - Linux
  - Open Source
  - opensource
  - peresonal
  - tools

---
 

## Lolcat-style photos as you commit

I&#8217;ve always had problems installing [lolcommits][1] on Xubuntu and other Ubuntu-based Linux distributions.

The installation instructions are very simple. Only requiring you to run two commands, sudo apt-get install mplayer imagemagick libmagickwand-dev and then sudo gem install lolcommits (need `sudo` for linux). Pretty simple.

The gem install lolcommits command is where things usually go bad for me. I typically see something like this:

<pre class="wp-block-preformatted">tyler@echo:~$ sudo gem install lolcommits
Building native extensions.  This could take a while...
ERROR:  Error installing lolcommits:
	ERROR: Failed to build gem native extension.

        /usr/bin/ruby1.9.1 extconf.rb
/usr/lib/ruby/1.9.1/rubygems/custom_require.rb:36:in `require': cannot load such file -- mkmf (LoadError)
	from /usr/lib/ruby/1.9.1/rubygems/custom_require.rb:36:in `require'
	from extconf.rb:1:in `&lt;main>'


Gem files will remain installed in /var/lib/gems/1.9.1/gems/oj-2.0.14 for inspection.
Results logged to /var/lib/gems/1.9.1/gems/oj-2.0.14/ext/oj/gem_make.out</pre>

To fix this, you need to install a newer ruby-dev package:

<pre class="wp-block-preformatted">sudo apt-get install ruby1.9.1-dev</pre>

You can now try to install the lolcommits gem again. It&#8217;ll actually install this time:

<pre class="wp-block-preformatted">gem install rdoc</pre>

<pre class="wp-block-preformatted">gem install lolcommits</pre>

A GitHub user [documented this solution][2] in [issue #54][3]. [Another user suggests][4] that the installation guide should be updated to make a note of this, but I haven&#8217;t seen it noted anywhere but in [issue #54][3].

It&#8217;d sure save me a bit of time if it was noted somewhere, that&#8217;s partly why I&#8217;m writing this post.

After you&#8217;ve got lolocommits installed, see [the README on GitHub][5] for usage instructions and examples.

I usually run `lolcommits --enable --delay=2 --fork` when enabling lolcommits. That will capture a photo in a forked process, after a 2 second delay. I like this method because you&#8217;re not left waiting for the photo before being able to type into your terminal again.

Lolcommits is kinda cool, but not really useful in a practical sense. I do use it pretty much everywhere though, and have the default storage location linked to [Copy][6]. That way all my images are in the same place, no matter which machine I&#8217;m using at home.

If nothing else, it&#8217;s something kinda neat to be able to offer to your clients.

<div class="wp-block-image">
  <figure class="aligncenter"><a href="https://i2.wp.com/longren.io/wp-content/uploads/2014/05/tyler-hat-lolcommits.jpg"><img loading="lazy" width="640" height="480" src="https://i2.wp.com/longren.io/wp-content/uploads/2014/05/tyler-hat-lolcommits.jpg?resize=640%2C480" alt="tyler-hat-lolcommits" class="wp-image-6857" srcset="https://i1.wp.com/www.longren.io/wp-content/uploads/2014/05/tyler-hat-lolcommits.jpg?w=640&ssl=1 640w, https://i1.wp.com/www.longren.io/wp-content/uploads/2014/05/tyler-hat-lolcommits.jpg?resize=150%2C112&ssl=1 150w, https://i1.wp.com/www.longren.io/wp-content/uploads/2014/05/tyler-hat-lolcommits.jpg?resize=300%2C225&ssl=1 300w" sizes="(max-width: 640px) 100vw, 640px" data-recalc-dims="1" /></a><figcaption> I no longer smoke. 😉</figcaption></figure>
</div>

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="6841"
					data-ulike-nonce="91deb0c0eb"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_6841"></button><span class="count-box"></span>
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

 [1]: https://github.com/mroth/lolcommits/
 [2]: https://github.com/mroth/lolcommits/issues/54#issuecomment-22554951
 [3]: https://github.com/mroth/lolcommits/issues/54
 [4]: https://github.com/mroth/lolcommits/issues/54#issuecomment-22758725
 [5]: https://github.com/mroth/lolcommits/blob/master/README.md
 [6]: https://copy.com?r=1XNUBL
 [7]: #