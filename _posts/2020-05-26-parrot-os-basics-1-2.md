---
layout: post
published: true
title: Parrot OS Basics 1.2
tags:
  - PWP
  - Beginner
  - Parrot OS Basics
comments: true
---
# Managing services in parrot

## Introduction

In this blog post, we will learn how to manage services and programs in Parrot OS.

## Linux Services

Linux services are the program that runs in the background outside the interactive control of the system.
Services also are known as daemons in Linux systems. example - sshd, httpd (d is for daemon).

We have to switch user to root to use sytemctl and service command (check the usage using 'man systemctl', 'man service'.

``
$ su ( to switch user to root)
``

Now list all the services using the command below
~~~
 # systemctl list-unit-files --type service --all

~~~
This command will show enable, disable. masked, static services

To know only running services
~~~
# systemctl | grep running
~~~

To start a service 
~~~
# service [service_name] start
~~~
or
~~~
# systemctl start [service_name]
~~~
To stop service
~~~
# systemctl stop [service_name]
~~~
or
~~~
service [service_name] stop
~~~
To know the service status
~~~
# systemctl status [service_name]
~~~
or
~~~
# service [service_name] status
~~~

It is also possible to have a service run while the operating system is being loaded:

~~~
# systemctl enable [service_name]
~~~
or
~~~
# service [service_name] enable
~~~

To disable service
~~~
# systemctl disable [service_name]
~~~
or
~~~
# service [service_name] disable
~~~

## Conclusion

_**This is the high-level overview to system services and how to manage them..**_
