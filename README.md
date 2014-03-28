zabbix-iptstate
===============

Simple Zabbix template for displaying states of network connections inside your Linux box.

Requisites

-iptstate package
-sudo permission for zabbix user to run iptstate

Instation

-Make sure that in your /etc/init.d/zabbix_agent.conf there is an include for the /etc/zabbix/zabbix_agent.d folder
-Download the UserParameter file and place it to /etc/zabbix/zabbix_agent.d/
-Add the following line to sudoers

  zabbix  ALL=NOPASSWD: /usr/sbin/iptstate

-Import the template on the web interface

Job done enjoy.
