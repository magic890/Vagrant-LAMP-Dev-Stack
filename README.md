# Vagrant LAMP Dev Stack

## Requirements
* [VirtualBox](https://www.virtualbox.org)
* [Vagrant](http://vagrantup.com)
* [Berkshelf](http://berkshelf.com)
	* `gem install berkshelf`
* [vagrant-berkshelf](https://github.com/riotgames/vagrant-berkshelf)
	* `vagrant plugin install vagrant-berkshelf`
* [vagrant-hostmanager](https://github.com/smdahlen/vagrant-hostmanager)
	* `vagrant plugin install vagrant-hostmanager`

## Installation
Clone this repository

    $ git clone git@github.com:magic890/Vagrant-LAMP-Dev-Stack.git

Place your website in the `public` folder.

## Usage
Start the VM

	$ cd Vagrant-LAMP-Dev-Stack
	$ vagrant up

You can now access your project at [http://projectname.local](http://projectname.local)

![Screenshot of up-and-running server](http://i.imgur.com/TP1i9Zd.png)

### Database dump import (Optional)
Chef will automatically try to import the database dump specified by the filename set in the `:db_dump` option of your Vagrantfile.
It must be placed in `public` folder.

## Installed software
* Apache 2
* MySQL
* PHP 5.4 (with mysql, curl, mcrypt, memcached, gd)
* memcached
* postfix
* vim, git, screen, curl, composer

## Default credentials
### MySQL
* Username: root
* Password: `database_password`
* Host: `ip_address`
* Port: 3306

**Note:** Remote MySQL access is enabled by default, so you can access the MySQL database using your favorite MySQL client with the above credentials (and using e.g. *projectname.local* as hostname).

### Memcached
* Port: 11211



