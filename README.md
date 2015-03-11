#Zabbix-iptstate

Simple Zabbix template for displaying states of network connections inside your Linux box.

## Installation

 - Install the iptstate package

 ```shell
 sudo apt-get install ipstate
 ```
 - Make sure that in your /etc/init.d/zabbix_agentd.conf there is an include for the /etc/zabbix/zabbix_agentd.conf.d
 
 ```shell
 augtool -s set /files/etc/zabbix/zabbix_agentd.conf/Include "/etc/zabbix/zabbix_agentd.conf.d/"
 ```
 - Download the UserParameter file and place it to /etc/zabbix/zabbix_agent.d/

 ```shell
 wget -P /etc/zabbix/zabbix_agentd.conf.d https://raw.githubusercontent.com/kisst/zabbix-iptstate/master/userparameter_iptstate.conf
 ```
 - Add the following line to sudoers

 ````shell
  zabbix  ALL=NOPASSWD: /usr/sbin/iptstate
 ```
 - reload the zabbix agent
 - Import the template on the web interface

Job done enjoy it!

