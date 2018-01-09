
Github: https://github.com/kresimir71/gigs

Introduction
################################

What is it about?
*************************

This is a list of competencies I am able to offer according to your needs.

How does it work?
*********************************

A list containes a short description for each functionality you can be interested in. It should give a basic picture of how does it work for me and how it could work for you.

What kind of copyright do you get?
====================================================

The software you receive will usually be licensed by a license equivalent to the MIT free software license. (Except when that is not possible because already derived from e.g. GPL licensed software).

Excuses
*********************************

Apologises for taking a global name 'gigs' at 'readthedocs' for my private offer - it happened before I was aware of it.

Furnishing web server with linux packages
##################################################

Begin with a freshly installed Linux server. The scripts will install a sound combination of packages needed for the function of

* firewall
* load balancer
* development
* database
* webserver

The input to the scripts will be:

* login credentials
* IP address
* host name

The scripts can be deployed many times for each new server again.

Making backup with rsync
#################################################################

Copy the required directories from one source linux system to another destination one through a secure connection. Copy only the changed files and maintain the backup directories on the destination system. E.g. for hourly backups you get copies on the destination:

.. code-block:: guess

 dir2018-02-01-07
 dir2018-02-01-06
 dir2018-02-01-05
 dir2018-02-01-04

Any of the copies containes all source files, also the unchanged ones (by using hard links). It is possible to delete any of the copies separately,e.g.:

.. code-block:: guess

 rm -rf dir2018-02-01-05 # remove copy made at 5AM

without affecting the other ones.

There is an option to stop specified services on the source system during the process. There is also an option to schedule restart of the stopped services on the source system in the case of the destination system failure (e.g. power off).

The scripts are generic and easy to maintain.

SSL certificates with letsencrypt
#################################################################

With letsencrypt, the free SSL provider, it is possible to get SSL certificates for the main domain name and any needed subdomains. 

The key and certificate files are concatinated to one file per domain or subdomain name and all put in one directory which can directly be used by the web server (i.e. apache) or load balancer (i.e. haproxy).
 
The renewal is scheduled and is automated.

Obtaining domainname and SSL for volatile IP addresses
#########################################################

Your IP address at home is not fixed but subject to change as needed by your internet provider. It could change once per year or every month, on average.

This unit helps you to obtain and maintain a domainname which points to your home IP address regardless of how often the IP address changes. It also immediatelly installs a new SSL certificate so your system at home can be accessed via a secure connection.

The renewal of SSL certificate is automated.

The system monitors its IP address and when it changes, the scripts change the DNS records to point to the new IP address and also obtain a new SSL certificate.

Liquid cooling of your computer system
#############################################################

With the current internet speeds available also at home it becomes feasible to have an internet server at home. With liquid cooling the system is likely to have less impact on your home environment.

Google Adwords
#############################################################

This is a way of promoting a website by using Google advertising. For a small amount of money payed per click to Google, when the amount is higher than what other users have payed for the same keywords, your site advertisement will be highlighted in the search results. The utility is very convenient because you can also see how often your site has been shown to the customers of the search engine: "An impression is counted each time your ad is served on Google's ad networks". Google provides free of charge online coaching for beginners.

Setting DNS record by a script
################################################################

Suppose there is a new domainname or an old domainname for which you need to change the DNS record so that it points to an IP address. It is convenient to configure the DNS record by using a script. Input to the script is the domainname and the IP address of the server to point to. If the required subdomain does not exist yet, it will be created.

Emacs tags
############################################################

The classical programmers editor Emacs (and XEmacs) has the possibility to search in the source files for the name of variables and functions. The shell 'etags' utility is used to index the given files and directories. 'etags' has built in syntax recognition for the most languages. Besides that I use a lot what we can call 'custom tagging'. For instance I choose the name for TAG, like TAG1 and mark the interesting places in the source files like:

.. code-block:: guess

 // TAG1(bash_shell_some_interesting_snippet)

The same tag is listed in an index file, e.g. index.txt:

.. code-block:: guess

 // TAG1(bash_shell_some_interesting_snippet)

This gives the possibility to jump from index.txt within emacs to all occurrences of a given tag.

Sending email from your server
############################################################

Contrary to what common opinion could be, sending email from your server is not a trivial problem because there can be receivers which will clasify the IP address of your server as a possible SPAM source. The suggested solutions here are 'Turbosmtp' and 'Google mail' e-mail sending providers. There are also excelent Wordpress plugins specialised in these two providers. I would suggest configuring a *dedicated server for relaying the mail* of all your other servers to the e-mail sending provider.

GNU automake system
############################################################

GNU automake is a sofisticated configuration and build system for usage with C/C++ sources and also any other programming language in order to make, test, organize, distribute, build, install a software project.

One recent project in which I have used 'GNU automake' is http://libkk71swigphp.readthedocs.io . It is about using C++ libraries from PHP. It works in WordPress!

Boilerplate templates in m4 and php
############################################################

Boilerplate templates is my favourite trick. The languages used are m4,php,emacs lisp, but the best results are achieved by a combination of them.

ttt templates
***************************************************************

This is a suite of scripts that processes boilerplate templates written in php. It works like this:

The utility takes a directory tree of template files of three sorts:

.. code-block:: guess

 path/name
 path/name.phptt
 path/name.php.phptt

where 'path' and 'name' can also be string templates like

.. code-block:: guess

 dir1_{ttt_var1}/dir2_{ttt_var2}/file_{ttt_var3}.txt.phptt

where the variables like 'ttt_var1' will be defined in the shell script settings.sh which is an input to the processing. The prefix 'ttt_' for the variables is required.

The files of the form 

.. code-block:: guess

 path/name.php.phptt

will be processed by 'php' by using 

.. code-block:: guess

 require 'settings.php' 

first, where settings.php is an input configuration file to the process. The result will be the file

.. code-block:: guess

 path/name.php

in which a search/replace will be done:

.. code-block:: guess

 >?php with <?php and ?< with ?>

(That defines how template that has to result in php source is processed: php template which produces php!)

The files of the form 

.. code-block:: guess

 path/name.phptt

will be processed by 'php' by using 

.. code-block:: guess

 require 'settings.php' 

first, where settings.php is an input configuration file to the process. The result will be the file

.. code-block:: guess

 path/name

The other files which do not have .phptt extension suffix will not be processed and will be left as they are.

Example: Wordpress customizer snippets
====================================================================

It is about programming 'the customizer', a submenu of the WordPress admin menu.

Note that the templates here are php templates which also produce php code!

WordPress websites in Upfront
############################################################

Upfront is an extremly user-friendly editor for creating modern
responsive websites in Wordpress, provided by WPMUDEV.

Protecting the server by rejecting ip addresses in firewall
#################################################################

Firewall on linux systems is realised by iptables. By allowing only
selected set of IP addresses to make connection from outside, you can
work on a website in private without possibility of access from other
IP. Or you can use this facility to close SSH port and so keep your
logs clean of bots trying to log in.

In all cases there are secret URLs configured on the server with one
purpose: a hit to that URL makes the connecting source IP
allowed. Manual adding of an IP is also possible.

Creating documentation with Sphinx
##############################################################

Sphinx is a simple way of writing documents. The input is very much
readable: that's very good for version control (i.e. git) because you
can easily see the changes made.

After all this site has been made in Sphinx.
For an example of input document, see the input of this document:

http://gigs.readthedocs.io/en/latest/_sources/gigs.rst.txt

There are many good, free of charge Sphinx courses to be found on internet, just type:

 youtube python sphinx

in your favourite best search engine in the world.

You get PDF, HTML, Epub output formats. When the source is on 'github'
then an automatic output appears on 'readthedocs' site. You can also
have your own, local, internal, secured, safe 'readthedocs' server for
your company documents created from your secure local repositories.

Video surveillance site
##############################################################

Offered is a complete software and documentation for installation,
usage and maintenance of a camera surveillance site like:

https://camera.stand71.click

with or without online shop. In this
manner you can manage your own surveillance site on your own server,
hosting hundreds of cameras, excluding the danger that the other parties
will watch your videos. Supported are all cameras sending images to a
ftp server.

An example of a camera surveillance site with the fresh videos of the
recent days can be found on the example site. It is about securing the barn of
my house.  You need a camera that can send images by the FT protocol
to the server. Than on the server the images you send are used to
produce hourly and daily videos. If your camera has motion detection
then you should turn that facility on and have picture only when there
is some action. If your camera does not have motion detection then I
have some ongoing development to show only motion in the videos
anyway. 

Multiple websites using one PayPal account
##############################################################

PayPal only allows you to set a single IPN URL and that limits its use to a single website. If you want to receive payments via PayPal on multiple websites then you need to put a special script on one of your domains, as an IPN URL in paypal you put the URL of that script and finally in that script you add your "real" IPNs from your various sites (any other domain of yours) that need to receive IPN calls.

That is the solution I have implemented and tested successfully. 

.. API
.. ********************************

.. Tutorial
.. *******************
