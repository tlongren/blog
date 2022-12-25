---
title: Hi-Ho, It’s Off to Work We Go
author: Tyler Longren
type: post
date: 2005-06-06T13:45:27+00:00
url: /hi-ho-its-off-to-work-we-go/
views:
  - 1104
dsq_thread_id:
  - 1385912383

---
I&#8217;ve not been very active with this site during the last week. There&#8217;s lots of stuff going on at work, some of which I will discuss here. As some of you know, I setup an order verification system a couple months ago. I&#8217;ve been doing a whole lot more work on that lately. I had to be to our warehouse in Ankeny at 7:00AM on Saturday.

Anyway, we&#8217;ve purchased a couple more scanning systems. I&#8217;ve almost got two stations in production now. I still have to program a few features into the second flatbed scanner, but that&#8217;s no problem. Probably will do that some time today.

I&#8217;ll probably start setting up the third and final scanning station sometime today. I&#8217;ve also setup a database server in the office in Ankeny. It&#8217;s running [Slackware 10.1][1], [kernel 2.4.30][2], and [MySQL 4.1.12][3]. It serves all the order data for the verification stations.

That database server is located almost a 1/4 mile away from the actual scanning stations. I setup a wireless network in the cooler/warehouse last week also. I purchased a few [Linksys WUSB54G wireless cards][4] for the scanning PC&#8217;s. I absolutely love those cards, I even picked one up for myself at home.

Having the database server in place makes my life so much easier. Previously, I&#8217;d have to e-mail the order verification data to our warehouse manager nightly and depend on him to upload it. He wouldn&#8217;t always upload it and I&#8217;d end up getting in trouble. I setup a nice web frontend to the database server. Once our browsers are pointed to the database server, we just select the file that contains the orders from our desktop and upload them to the db server right through a web browser. I don&#8217;t have to worry about other people doing their jobs anymore.

Previously, the database was running on the actual verification system. I wanted to have a central place for all the data since we decided to add a couple more scanning stations. I didn&#8217;t want one of the verification systems hosting all the data and having the warehouse guys worry about which PC&#8217;s they have on. The way it is now, the only machine they have to worry about turning on is the one they choose to verify orders with.

We also re-designed the scanning &#8220;table&#8221;. It&#8217;s much better now. Before there wasn&#8217;t much room for them to set their pre-picked food. Now there&#8217;s plenty of room. We also purchased LCD monitors for all the stations. They look really slick now. I&#8217;ll probably take a couple pictures later on in the week.

So, that&#8217;s been the story of my life for the last week. I don&#8217;t expect I&#8217;ll have to work as much this week as I&#8217;ve got most of the hard work done now.

Yesterday, Ashley and I went to Hickory Grove. It&#8217;s a little local lake. We just sat out there for about an hour or so. It was really nice out but way too damn windy. Supposed to get up to 90 degrees today. First time it&#8217;s been this warm since August of last year. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="1910"
					data-ulike-nonce="6f174e0173"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_1910"></button><span class="count-box"></span>
  </div>
</div>

[][5]{.later-button-el}

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

 [1]: http://www.slackware.com/
 [2]: http://www.kernel.org/
 [3]: http://dev.mysql.com/
 [4]: http://www.linksys.com/products/product.asp?grid=33&scid=36&prid=578
 [5]: #