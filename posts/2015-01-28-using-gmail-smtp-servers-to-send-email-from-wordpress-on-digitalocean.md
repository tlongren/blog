---
title: Using Gmail SMTP Servers to Send Email From WordPress on DigitalOcean
author: Tyler Longren
type: post
date: 2015-01-28T13:24:53+00:00
url: /using-gmail-smtp-servers-to-send-email-from-wordpress-on-digitalocean/
featured_image: /wp-content/uploads/2015/01/wpdo.png
independent_publisher_primary_category:
  - DigitalOcean
dsq_thread_id:
  - 3463016480
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - cool
  - digitalocean
  - hosting
  - Internet
  - Noteworthy
  - PHP
  - tutorials
  - WordPress

---
## Use Gmail SMTP Servers for Sending Emails from WordPress

After quite a bit of back and forth between sendmail, postfix, and exim, I&#8217;ve settled on using [msmtp][1] for sending emails from my servers/droplets at [DigitalOcean][2] (affiliate link). 

MSMTP is very lightweight and has the ability to send emails via an existing SMTP server, like Gmail&#8217;s or Yahoo&#8217;s.

To get it working, there&#8217;s a few tricks. I&#8217;ve pieced this together from [this post][3] and [this post][4]. And when on DigitalOcean, there&#8217;s an IPv6 issue that causes major delays in sending the email, which there&#8217;s a fix for at the end of this post.

### 1. Install msmtp

<pre class="wp-block-preformatted">sudo apt-get install msmtp</pre>

### 2. Configure msmtp to use Gmail

Open up `/etc/msmtprc` as root: sudo nano /etc/msmtprc, and add the following, removing whatever else is there: 

<pre class="wp-block-preformatted"># Gmail/Google Apps
account  gmail 
host   smtp.gmail.com 
port   587 
from   example@gmail.com
user   example@gmail.com
password  enter-password-here!
auth   on 
tls   on 
tls_trust_file /etc/ssl/certs/ca-certificates.crt 
 
# Default account to use
account default : gmail</pre>

You&#8217;ll want to replace the `user` directive with a valid Gmail email address, a Gmail account or a Google Apps email address will work, too. Don&#8217;t forget to change `enter-password-here!` to the actual password for the Gmail account your using.

Save `/etc/msmtprc`.

### 3. Remove Sendmail

Run this: 

<pre class="wp-block-preformatted">sudo apt-get remove sendmail-bin</pre>

### 4. Setup Some Aliases

Lots of software on Linux systems uses the sendmail command. Instead, we&#8217;re using msmtp, so we&#8217;re essentially invoking msmtp when the `sendmail` command is run. 

<pre class="wp-block-preformatted">sudo ln -s /usr/bin/msmtp /usr/sbin/sendmail
sudo ln -s /usr/bin/msmtp /usr/bin/sendmail
sudo ln -s /usr/bin/msmtp /usr/lib/sendmail</pre>

### 5. Tell PHP About msmtp

First, locate your `php.ini` file that&#8217;s being used by Apache. It&#8217;s typically in `/etc/php5/apache2/php.ini`. If that&#8217;s not it, use PHP&#8217;s `phpinfo()` function to find the location of your `php.ini` file.

Find `sendmail_path =` in `php.ini` and replace it with this: 

<pre class="wp-block-preformatted">sendmail_path = "/usr/bin/msmtp -t"</pre>

Now you should be able to send mail using PHP&#8217;s mail() function, which will use the Gmail SMTP server to send emails. Add this to a PHP file and access it through your browser to see if it works: 

<pre class="wp-block-preformatted">&lt;?php
if(mail("receipient@domain.com","A Subject Here","Hi there,nThis email was sent using PHP's mail function."))
print "Email successfully sent";
else
print "An error occured";
?></pre>

### 6. Disable IPv6 If You Experience Slowness

Open up `/etc/gai.conf` like so: 

<pre class="wp-block-preformatted">sudo nano /etc/gai.conf</pre>

Now, look for a line that looks like this: `#precedence ::ffff:0:0/96 100`. Uncomment that line (remove the #) and save `/etc/gai.conf`. An explanation of why this helps can be found in [this comment][5] at the [DigitalOcean article][4].

### All Done

That should be it. If you run into any issues please do leave a comment, I&#8217;ll do my best to help you out. I may have missed a part, so no guarantees this will work for you. It does however work wonderfully on a [DigitalOcean][2] droplet that&#8217;s running Ubuntu 14.04 with a pretty standard LAMP stack.

You should now be able to send email from WordPress on DigitalOcean.

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="7885"
					data-ulike-nonce="3aed558ceb"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_7885"></button><span class="count-box"></span>
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

 [1]: http://msmtp.sourceforge.net/
 [2]: https://www.digitalocean.com/?refcode=cbf49d0481c8
 [3]: http://netfactory.dk/2014/01/06/sending-mail-from-a-droplet/
 [4]: https://www.digitalocean.com/community/tutorials/how-to-use-gmail-or-yahoo-with-php-mail-function
 [5]: https://www.digitalocean.com/community/tutorials/how-to-use-gmail-or-yahoo-with-php-mail-function?comment=14581
 [6]: #