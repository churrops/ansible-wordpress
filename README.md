<h1> ANSIBLE WORDPRESS INSTALL </h1>

Description: Wordpress setup using Ansible

Pre requisites:

 - RHEL/CentOS
 - Apache Httpd
 - MariaDB

Clone git repository, and access the project

<pre>git clone https://github.com/churrops/ansible-wordpress.git
cd ansible-wordpress</pre>

Variables

You can change the variables for wordpress

<pre>cat group_vars/all</pre>

<h3> Staging Deploy </h3>

Edit the inventory file with our staging server

<pre>$ cat inventories/stg/hosts
[dbservers]
192.168.100.104

[webservers]
192.168.100.104
</pre>

Run deploy

<pre>./deploy.sh stg</pre>

<h3> Production Deploy </h3>

Edit the inventory file with our staging server

<pre>$ cat inventories/prd/hosts
[dbservers]
192.168.100.104

[webservers]
192.168.100.104
</pre>

<pre>./deploy.sh prd</pre>
