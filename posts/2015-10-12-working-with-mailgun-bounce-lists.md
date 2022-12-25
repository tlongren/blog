---
title: Working with Mailgun Bounce Lists
author: Tyler Longren
type: post
date: 2015-10-12T12:35:06+00:00
url: /working-with-mailgun-bounce-lists/
featured_image: /wp-content/uploads/2015/10/mailgun-wp.png
independent_publisher_primary_category:
  - Internet
dsq_thread_id:
  - 4217024343
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cool
  - Internet
  - Linux
  - mailgun
  - Noteworthy
  - Personal
  - services
  - tools
  - tutorials
  - WordPress

---
 

## Manipulate Mailgun Bounce Lists: Show, Add, and Delete Email Addresses. All from the terminal.

I recently came across a situation where a client reached their disk usage limit. As a result, they were unable to receive emails. This went un-noticed for a couple days (I didn&#8217;t manage the server at the time, I do now).

This client has a couple different WordPress sites with several employees receiving various notification emails. All their sites use [Mailgun][1] and the [Mailgun WordPress plugin][2] for sending emails. During the time they were unable to receive email, a few employee email addresses got placed on a [Mailgun bounce list][3] with a status of [550 Administrative prohibition][4].

For some background, here&#8217;s how Mailgun describes a bounce, as found [in the Mailgun documentation][3]:

<blockquote class="wp-block-quote">
  <p>
    Bounce list stores events of delivery failures due to permanent recipient mailbox errors such as non-existent mailbox. Soft bounces (for example, mailbox is full) and other failures (for example, ESP rejects an email because it thinks it is spam) are not added to the list.
  </p>
  
  <p>
    Subsequent delivery attempts to an address found in a bounce list are prevented to protect your sending reputation.
  </p>
</blockquote>

<div class="wp-block-image">
  <figure class="aligncenter"><a href="https://i1.wp.com/longren.io/wp-content/uploads/2015/10/mailgun-bounced.png?ssl=1"><img loading="lazy" width="1024" height="480" src="https://i1.wp.com/longren.io/wp-content/uploads/2015/10/mailgun-bounced-1024x480.png?resize=1024%2C480" alt="mailgun-bounced" class="wp-image-8182" srcset="https://i1.wp.com/www.longren.io/wp-content/uploads/2015/10/mailgun-bounced.png?resize=1024%2C480&ssl=1 1024w, https://i1.wp.com/www.longren.io/wp-content/uploads/2015/10/mailgun-bounced.png?resize=150%2C70&ssl=1 150w, https://i1.wp.com/www.longren.io/wp-content/uploads/2015/10/mailgun-bounced.png?resize=300%2C141&ssl=1 300w, https://i1.wp.com/www.longren.io/wp-content/uploads/2015/10/mailgun-bounced.png?resize=700%2C328&ssl=1 700w, https://i1.wp.com/www.longren.io/wp-content/uploads/2015/10/mailgun-bounced.png?w=1641&ssl=1 1641w" sizes="(max-width: 1024px) 100vw, 1024px" data-recalc-dims="1" /></a></figure>
</div>

I first noticed the bounce issue in the logs, like in the image below. After not being able to find a way to manage email addresses on the bounce list from the browser, I hit up Google and was pleased to find that you can interact with Mailgun bounce lists via their API.  


#### Show Email Addresses in the Mailgun Bounce List

To list email addresses on the bounce list, do something like this on the terminal/command line, replacing _key-xxx-xxx_ with your actual Mailgun API key:

<pre class="wp-block-preformatted">curl -s --user 'api:key-xxx-xxx' -G https://api.mailgun.net/v3/mg.longrendev.io/bounces</pre>

<div class="wp-block-image">
  <figure class="alignleft"><a href="https://i1.wp.com/longren.io/wp-content/uploads/2015/10/json-prettifier.png?ssl=1"><img loading="lazy" width="150" height="125" src="https://i0.wp.com/longren.io/wp-content/uploads/2015/10/json-prettifier-150x125.png?resize=150%2C125" alt="json-prettifier" class="wp-image-8190" srcset="https://i2.wp.com/www.longren.io/wp-content/uploads/2015/10/json-prettifier.png?resize=150%2C125&ssl=1 150w, https://i2.wp.com/www.longren.io/wp-content/uploads/2015/10/json-prettifier.png?resize=300%2C250&ssl=1 300w, https://i2.wp.com/www.longren.io/wp-content/uploads/2015/10/json-prettifier.png?resize=700%2C583&ssl=1 700w, https://i2.wp.com/www.longren.io/wp-content/uploads/2015/10/json-prettifier.png?w=985&ssl=1 985w" sizes="(max-width: 150px) 100vw, 150px" data-recalc-dims="1" /></a></figure>
</div>

You can find your Mailgun API key on [the Mailgun dashboard][5], under API Keys. The Mailgun API will return JSON, which is a bit difficult to read in the terminal. I usually copy the output and paste it into [this JSON formatter][6], which makes the data much easier to read, as you can see in the screenshot above.

Even when the formatted JSON in it&#8217;s raw form is easier to read. See, here&#8217;s the returned JSON, in it&#8217;s original form:  
<figure class="wp-block-embed">

<div class="wp-block-embed__wrapper">
  <div class="oembed-gist">
    <noscript>
      View the code on <a href="https://gist.github.com/tlongren/7697704d62f26235661e">Gist</a>.
    </noscript>
  </div>
</div></figure> 

Now here&#8217;s the pretty, formatted JSON as raw text:  
<figure class="wp-block-embed is-type-rich is-provider-embed-handler">

<div class="wp-block-embed__wrapper">
  <div class="oembed-gist">
    <noscript>
      View the code on <a href="https://gist.github.com/tlongren/7697704d62f26235661e">Gist</a>.
    </noscript>
  </div>
</div></figure> 

Much easier to read, right? Those of you using REST clients like [Postman][7] will have your results automatically prettified, removing the need using a site like [the JSON formatter][6] I typically use.

#### Delete an Email Address from the Mailgun Bounce List

If you&#8217;ve found an email address you&#8217;d like to remove from the Mailgun bounce list, or already know the email you want to remove, do this from a terminal and replace _email@somedomain.com_ with the real email address to delete. And of course, replace _key-xxx-xxx_ with your actual Mailgun API key:

<pre class="wp-block-preformatted">curl -s --user 'api:key-xxx-xxx' -H "Accept: application/json" -X DELETE https://api.mailgun.net/v3/mg.longrendev.io/bounces/email@somedomain.com</pre>

#### Add an Email Address to the Mailgun Bounce List

Sometimes you may wish to manually add an email address to the Mailgun bounce list. This can be done very easily with the CURL command below. It will add _email@somedomain.com_ to the Mailgun bounce list, so make sure to change that to the email you really want to add to the list.

<pre class="wp-block-preformatted">curl -s --user 'api:key-7g0wl66k2hxonzq5-0nbzhw68r2oc8n8' https://api.mailgun.net/v3/mg.longrendev.io/bounces -F address='email@somedomain.com'</pre>

#### What Else?

Not much concerning Mailgun bounce lists specifically. It&#8217;s possible to add multiple addresses to a bounce list at once, but that gets a little more difficult from the terminal as it requires sending JSON to the Mailgun API. Using a client like [Postman][7] would be a better option if you intend on sending much data.

The Mailgun API can be used to do all sorts of stuff, like pull stats and to create new domains. It&#8217;s a powerful API and one of my favorites to work with.

<div id="polls-33" class="wp-polls">
</div>

<div id="polls-33-loading" class="wp-polls-loading">
  <img src="https://i2.wp.com/www.longren.io/wp-content/plugins/wp-polls/images/loading.gif?resize=16%2C16&#038;ssl=1" width="16" height="16" alt="Loading ..." title="Loading ..." class="wp-polls-image" data-recalc-dims="1" />&nbsp;Loading ...
</div>

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="8181"
					data-ulike-nonce="d2157c9135"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image image-unlike wp_ulike_btn_is_active wp_likethis_8181"></button><span class="count-box">9+</span>
  </div>
</div>

[][8]{.later-button-el}

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

 [1]: http://mailgun.com
 [2]: https://wordpress.org/plugins/mailgun/
 [3]: https://documentation.mailgun.com/api-suppressions.html#bounces
 [4]: http://kb.mozillazine.org/Administrative_Prohibition
 [5]: https://mailgun.com/app/dashboard
 [6]: https://jsonformatter.curiousconcept.com/
 [7]: https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop?hl=en
 [8]: #