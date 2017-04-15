
Github: https://github.com/kresimir71/gigs

Introduction
################################

What is it about?
*************************

This is a list of competencies I am able to offer according to your needs.

How does it work?
*********************************

A list containes a short description for each functionality you can be interested in. It should give a basic picture of how does it work for me and how it could work for you.

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


.. API
.. ********************************

.. Tutorial
.. *******************
