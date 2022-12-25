---
title: The FEDERATED MySQL Storage Engine
author: Tyler Longren
type: post
date: 2006-08-24T20:15:18+00:00
url: /the-federated-mysql-storage-engine/
views:
  - 8338
ratings_users:
  - 4
ratings_score:
  - 12
ratings_average:
  - 3
wjt_diPostTopic:
  - linux_unix
diggURL:
  - http://www.digg.com/linux_unix/Linking_2_MySQL_Tables_Together
dsq_thread_id:
  - 1385931746
pageViews:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
pageViews_cumul:
  - '{"hours":{"1":"","2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":"","25":"","26":"","27":"","28":"","29":"","30":"","31":"","32":"","33":"","34":"","35":"","36":"","37":"","38":"","39":"","40":"","41":"","42":"","43":"","44":"","45":"","46":"","47":""},"days":{"2":"","3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":""},"weeks":{"3":"","4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":""},"months":{"4":"","5":"","6":"","7":"","8":"","9":"","10":"","11":"","12":"","13":"","14":"","15":"","16":"","17":"","18":"","19":"","20":"","21":"","22":"","23":"","24":""}}'
tags:
  - coding
  - data
  - databases
  - dba
  - development
  - mysql
  - programming
  - sql
  - storage

---
[The FEDERATED MySQL storage engine][1] is the coolest thing EVER! Seriously. It&#8217;s already saved me from having to do a whole bunch of synchronization coding. I can only imagine how it&#8217;ll come in useful in the future.

So, here&#8217;s my situation. I have two mysql servers sitting behind a firewall at &#8220;location 1&#8221;. People at &#8220;location 2&#8221; need to write some software to connect to both mysql servers at location 1. However, [MyODBC][2] gets confused when connecting to the same hostname on two different tcp ports, or so I&#8217;m told.

Anyway, since I was basically told that there&#8217;s no way to connect to two seperate mysql servers behind one firewall, I got to thinking. So, I set off searching google for method for mirroring data in MySQL and came across [the FEDERATED storage engine][1].

Now, the servers at location 1 are on a VPN with the network at location 3, my location. So, my network (at location 3) can see the network at location 1 without the firewall getting in the way. Since that&#8217;s the case here, I can connect to the default mysql port, 3306, on both servers because I can see their LAN IP, where the people at location 2 can&#8217;t (no VPN).

So, we&#8217;ve got the network flow figured out, now we can go about getting the FEDERATED storage engine in MySQL working. First, you&#8217;ll need [MySQL 5.x][3]. I chose MySQL 5.0.24 as it&#8217;s the latest stable 5.x release.

To enable the FEDERATED storage engine in mysql 5, you must pass the **&#8211;with-federated-storage-engine** option when running configure. That&#8217;s pretty much all that&#8217;s required to start using the FEDERATED storage engine. Most linux distributions probably have a mysql 5 package that comes with the FEDERATED engine on already, although Slackware does not currently.<!--more-->

  
<!--adsense-->

  
After you build mysql to support the FEDERATED storage engine, there&#8217;s really very little left to do to start making use of it. First you&#8217;ll need the table structure of the table you want to link to. We&#8217;ll use a table named &#8220;customers&#8221; as an example, with 3 fields, custId, fName, lName. The SQL used to build the initial &#8220;customers&#8221; table is below. The &#8220;customers&#8221; table is in the &#8220;companyData&#8221; database on the 192.168.1.248 MySQL server.

<pre>CREATE TABLE `customers` (
	`custId` int(10) unsigned NOT NULL default '0',
	`fName` varchar(100) default NULL,
	`lName` varchar(100) default NULL,
	PRIMARY KEY  (`custId`)
)
ENGINE=InnoDB
DEFAULT CHARSET=latin1;</pre>

A pretty simple and very basic table setup. Now, the SQL above is the SQL that&#8217;s used to generate the original table, the one that is actually storing all the data. To create a FEDERATED table that links to the original customers table, we use basically the same SQL, except we need to change a few things on the last couple lines:

<pre>CREATE TABLE `customers` (
	`custId` int(10) unsigned NOT NULL default '0',
	`fName` varchar(100) default NULL,
	`lName` varchar(100) default NULL,
	PRIMARY KEY  (`custId`)
)
ENGINE=FEDERATED
DEFAULT CHARSET=latin1
CONNECTION='mysql://mysqluser:mysqlpass@192.168.1.248:3306/companyData/customers';</pre>

See the last line there, the one starting with CONNECTION? That&#8217;s the real important one. It tells the new FEDERATED table where it needs to link to to get it&#8217;s data. The format of the CONNECTION clause is:

<pre>scheme://user_name[:password]@host_name[:port_num]/db_name/tbl_name</pre>

Pretty simple. You can read more about the FEDERATED storage engine [in the MySQL reference manual][4]. There&#8217;s also [a support forum dedicated][5] to the FEDERATED storage engine, as well as a [nice article over at the MySQL developer zone][6]. 

<div class="wpulike wpulike-default " >
  <div class="wp_ulike_general_class wp_ulike_is_not_liked">
    <button type="button"
					aria-label="Like Button"
					data-ulike-id="2224"
					data-ulike-nonce="63df2261d4"
					data-ulike-type="likeThis"
					data-ulike-template="wpulike-default"
					data-ulike-display-likers="0"
					data-ulike-disable-pophover="0"
					class="wp_ulike_btn wp_ulike_put_image wp_likethis_2224"></button><span class="count-box"></span>
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

 [1]: http://www.mysql.org/doc/refman/5.1/en/federated-storage-engine.html
 [2]: http://dev.mysql.com/downloads/connector/odbc/3.51.html
 [3]: http://dev.mysql.com/downloads/mysql/5.0.html
 [4]: http://www.mysql.org/doc/refman/5.0/en/federated-storage-engine.html
 [5]: http://forums.mysql.com/list.php?105
 [6]: http://dev.mysql.com/tech-resources/articles/mysql-federated-storage.html
 [7]: #