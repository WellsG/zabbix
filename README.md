# zabbix

### zabbix installation
[install from package](https://www.zabbix.com/documentation/2.2/manual/installation/install_from_packages)

#### zabbix server ( example on CentOS 7 )
````
zabbix22-server-mysql-2.2.16-1.el7.x86_64
zabbix22-2.2.16-1.el7.x86_64
zabbix22-dbfiles-mysql-2.2.16-1.el7.noarch
zabbix22-web-mysql-2.2.16-1.el7.noarch
zabbix22-server-2.2.16-1.el7.noarch
zabbix22-web-2.2.16-1.el7.noarch
````

#### configuration on zabbix server
start httpd and then visit:
http://<domain>/zabbix

[Config host/item/trigger](https://www.zabbix.com/documentation/2.2/manual/quickstart)

#### zabbix agent client ( example on fedora 22 )
````
zabbix-agent-2.4.7-1.fc22.x86_64
zabbix-2.4.7-1.fc22.x86_64
````


