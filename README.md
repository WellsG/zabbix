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
#### zabbix server's db configuration
````
DBName=zabbix
DBUser=zabbix
DBPassword=zabbix
````

#### start zabbix server
````
sudo zabbix_server start
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

#### zabbix agent config
/etc/zabbix_agentd.conf
````
Server=<IP addresses of Zabbix servers>
ServerActive=<IP addresses of Zabbix servers>
Hostname=<hostname configured on the server>
UserParameter=<key>, <shell command>
````

#### restart agentd after configuration, and verify if the key is worked on agent side (e.g: key: test.zabbix.key)
````
$ sudo zabbix_agentd start
$ zabbix_agentd -t test.zabbix.key
````
#### verify if the zabbix server side can get the value of the key
````
sudo zabbix_get -s <zabbix agent IP> -p 10050 -k 'test.zabbix.key'
````


