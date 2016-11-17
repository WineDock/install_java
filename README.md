# Ansible Role: install JRE
##scope
The scope of this Role is solely to install the JRE Package on your Server. It does enable you to choose the between available Versions.

##distributions

currently these Distributions are supported

 - CentOS 7 (Java 7 & 8)
 - Debian 8 (Java 7 & 8)
 - Ubuntu 10.04 (Java 7)
 - Ubuntu 12.04 (Java 7 & 8)
 - Ubuntu 14.04 (Java 7 & 8)
 - Ubuntu 16.04 (Java 7 & 8 & 9)

Extending is fairly easy and pull-requests are welcome. 
Maybe someone would like to add Debian 7 and Centos 6.

##tested distributions
I have tested on these distributions / Versions

 - CentOS 7
 - Debian 8
 - Ubuntu 16.04

##version variables

- javaversion

You might want to set these Variable in group_vars, as this helps moving from one version to another Version. 
default javaversion is 8 as per defaults/main.yml

##example playbook

	---
	- name: install bitbucket-server
	  hosts: bitbucket-server
	  become: true
	  become_user: root
	  roles:
	    - { role: "install_java",
	        javaversion: "8" 
	      }

## License
MIT / BSD

## Author Information
This role was created in 2016 by Wolfgang Wangerin at [Hawesko GmbH](http://www.hawesko.de)
