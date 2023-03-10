---
title: Keep Your Forked GitHub Repository In Sync
author: Tyler Longren
type: post
date: 2014-03-19T14:11:35+00:00
url: /keep-your-forked-github-repository-in-sync/
featured_image: /wp-content/uploads/2014/03/fork.png
dsq_thread_id:
  - 2439350019
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
independent_publisher_primary_category:
  - GitHub
tags:
  - git
  - GitHub
  - Internet
  - Open Source
  - opensource
  - Personal

---
## Fork something? Update your fork with changes from upstream

I fork a LOT of things I see on GitHub. It&#8217;s habit, most I never touch, but others I do keep up on.

It&#8217;s nice to be able to merge changes that the original authors made, back into my fork. Especially if a major feature was added in after I made my fork. Keeping your forked GitHub repository in sync with that of the original repository requires you to add a new git remote, merge the upstream code with your fork, and then push master back to your fork on GitHub.

### Here&#8217;s how it&#8217;s all done

First, you&#8217;ll need to add an `upstream` remote.

<pre class="wp-block-preformatted">git remote add upstream https://github.com/user/repo.git</pre>

There&#8217;s really only two steps involved. Fetching updates from the newly created `upstream` remote and then merging the changes into your code.

To fetch updates from the `upstream` remote, do this:

<pre class="wp-block-preformatted">git fetch upstream</pre>

Now we&#8217;ve got all the changes made to the original &#8220;forked&#8221; repository. All the changes are stored in a local branch, `upstream/master`. Neat!

Now, make sure you&#8217;re on the branch you&#8217;re supposed to be, if you don&#8217;t know, you want `master`. To ensure you&#8217;re on the local master branch, do this:

<pre class="wp-block-preformatted">git checkout master</pre>

Now that we&#8217;re on our local master branch, we can merge the changes from the original repository. To merge from the `upstream/master` branch to your local `master` branch, do this:

<pre class="wp-block-preformatted">git merge upstream/master</pre>

That&#8217;s it! You can now update your fork on GitHub with updates from the repository you originally forked.

<pre class="wp-block-preformatted">git push origin master</pre>

Now, at this point, your fork on GitHub should contain changes from the &#8220;original&#8221; repository that you forked, as well as any changes that you made to your own fork. Keep an eye on the &#8220;original&#8221; repository and perform these steps again, except for adding the `upstream` remote, you&#8217;ll only need to do that once.

For more information, checkout [this piece from GitHub Help][1].

<div id="polls-22" class="wp-polls">
</div>

<div id="polls-22-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="6095"
					data-ulike-nonce="63e1d222c0"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_6095"></button><span class="count-box">2+</span>
  </div>
</div>

[][2]{.later-button-el}

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
      Got a question or some updated information releavant to this post? Please, <a href='#respond' title='Leave a comment'>leave a comment</a>! The comments are a great way to get help, I read them all and reply to nearly every comment. Let's talk. ????
    </p>
  </div>
  
  <div class='now-what-bottom-ad'>
    <h3>
      Longren.io is proudly hosted by <a href='https://www.digitalocean.com/?refcode=cbf49d0481c8'>DigitalOcean</a>
    </h3>
    
    <span class='do_link'><a href='https://www.digitalocean.com/?refcode=cbf49d0481c8' rel='nofollow' target='_blank'><img alt='DigitalOcean' border='0' src='https://i0.wp.com/longren.io/wp-content/uploads/2014/03/digitalocean.png?w=1100&#038;ssl=1' data-recalc-dims="1" /></a></span> <!--<h3>Need Cloud Monitoring? Try Mist.io!</h3><span class='do_link'><a href='http://mist.io/?ref=tyler' rel='nofollow' target='_blank'><img alt='Mist.io' border='0' src='https://i0.wp.com/longren.io/wp-content/uploads/2014/04/mistio.jpg?w=1100&#038;ssl=1' data-recalc-dims="1"></a></span>-->
  </div>
</div>

 [1]: https://help.github.com/articles/syncing-a-fork
 [2]: #