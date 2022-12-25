---
title: Poor Man’s VPN With a Cheap VPS
author: Tyler Longren
type: post
date: 2014-04-14T14:45:39+00:00
url: /poor-mans-vpn-with-a-cheap-vps/
featured_image: /wp-content/uploads/2014/04/RSA_SecurID_SID80000.jpg
dsq_thread_id:
  - 2607591080
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
independent_publisher_primary_category:
  - Services
full_width_featured_image:
  - 1
tags:
  - cool
  - digital ocean
  - digitalocena
  - GitHub
  - Internet
  - Linux
  - Personal
  - services
  - ubuntu

---
## VPN using a cheap VPS and sshuttle

It really is awesome, [sshuttle][1] basically allows you to browse the web via your VPS, in my case, a [VPS from DigitalOcean][2] (sponsored link, as are the others to DigtialOcean). It works on Linux and MacOS.

The GitHub repo explains it better than I can.

<blockquote class="wp-block-quote">
  <p>
    Transparent proxy server that works as a poor man&#8217;s VPN. Forwards over ssh. Doesn&#8217;t require admin. Works with Linux and MacOS. Supports DNS tunneling.
  </p>
</blockquote>

It hasn&#8217;t been updated in two years, but, no need to fix or change something that doesn&#8217;t need fixing or changing.

### So, Why? What&#8217;s the point?

I [run some Tor relays][3], one [out of my house][4], thanks Mediacom! `;)`

Because of this, many websites block me. **Kohl&#8217;s**, **Best Buy**, no posting on 4Chan (understandable), even **healthcare.gov** is blocked. I don&#8217;t want to pay for one of the many VPN services. Here&#8217;s the message I get at healthcare.gov without sshuttle.

<blockquote class="wp-block-quote">
  <p>
    Access Denied
  </p>
  
  <p>
    You don&#8217;t have permission to access &#8220;http://www.healthcare.gov/&#8221; on this server.<br /> Reference #18.22ea4d17.1397361569.6bb6afe
  </p>
</blockquote>

VPN&#8217;s even provide vital Internet access to [those facing government censorship][5], and worse.

### Options

Setting up a secure VPN server on a linux box can be a pain, and definitely takes longer than 5 minutes. [sshuttle][1] takes about that, maybe, if you type really slow.

So, for me, when I found [sshuttle][1], my heart was set, the other options didn&#8217;t matter.

### Setting Up sshuttle On Ubuntu Flavors

Doesn&#8217;t get any easier than this. Run the following in a terminal:

<pre class="wp-block-preformatted">sudo apt-get install sshuttle</pre>

Now, we&#8217;re basically going to SSH to our VPS/server. Again, run this in the terminal:

<pre class="wp-block-preformatted">sshuttle -r username@vps.yourdomain.com 0/0 -vv</pre>

After running `sshuttle -r username@vps.yourdomain.com 0/0 -vv` you&#8217;ll be asked for the root password. And sometimes, for whatever reason, it dies immediately after running the `sshuttle` command.

**If sshuttle doesn&#8217;t work** after running it the first time, **run it again**! It should work the second time. It could be something with the system I&#8217;m on, so hopefully this is isolated to me. `:)`

### Setting Up sshuttle On MacOS

When someone donates me a new Macbook Pro 15&#8243;, I&#8217;ll start writing this stuff. `:)`  
**Update: April 21, 2014** [Have a look at this post for using sshuttle with MacOS][6]. Comes courtesy of [Aaron Bull Schaefer in the comments][7].

### And if I need a VPS?

You can find a [cheap VPS][2] easily with Google. [DigitalOcean has them for $5/month][2], which will be plenty sufficient to use specifically for [sshuttle][1].

[ChunkHost is another][8] good option for a cheap VPS.

### Other Options

Lots of other options have [been mentioned in the thread at Hacker News][9]. Check em out. Some really good suggestions that are sometimes even cheaper!

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="6484"
					data-ulike-nonce="f1775c7136"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_6484"></button><span class="count-box"></span>
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

 [1]: https://github.com/sshuttle/sshuttle
 [2]: https://www.digitalocean.com/?refcode=cbf49d0481c8
 [3]: http://longren.io/tor-is-important-for-privacy-and-the-internet/
 [4]: https://globe.torproject.org/#/relay/57E960AAB54DD590DC648C49AB12C1EACDCE5B6F
 [5]: http://www.geektime.com/2014/03/23/israeli-safer-social-offers-free-vpn-to-individuals-facing-government-censorship/
 [6]: http://elasticdog.com/2011/12/use-sshuttle-to-keep-safe-on-insecure-wi-fi/
 [7]: http://longren.io/poor-mans-vpn-with-a-cheap-vps/#comment-1342984268
 [8]: https://chunkhost.com/referral_codes/46053
 [9]: https://news.ycombinator.com/item?id=7586775
 [10]: #