Hello, everyone.
This script allows us to obtain complete Excel report which consist of two worksheets: 
information about all hosts from Zabbix Server and information about all templates from Zabbix Server.
![image](https://user-images.githubusercontent.com/106164393/207300210-95b7931f-5dbf-42e3-825b-09a84d2421ed.png)

The following are required for proceeding this script:
- python3
- modules:
sys
os
json
pyzabbix
getpass
openpyxl
platform
subprocess
time
datetime
collections
progress

How to?
To executing the script and get report you should run this and follow promts from python terminal:
- Add full Zabbix API path, such as: https://zabbixaddress/api_jsonrpc.php or https://zabbixaddress/zabbix/api_jsonrpc.php
- Type Zabbix API username
- Type Zabbix API user password
- Choose timeframes (from and till datetime in the format: 01/01/2000 00:00) for getting SLA info via hosts ICMP ping history
or press 'Enter' to set default values (30 days ago from the moment of script running)
- Select one of the options: get both hosts and templates info ('y') or only hosts information ('n') and press 'Enter'.

Then you may drink coffee or tea while waiting for the script execution.
The proceeding time depends on the number of unavailable hosts (ping response), the number of hosts and templates.

P.S. This is my second Python script and the first one concerned with Zabbix API.
So if you would like to modernize, optimize and make it better you are welcome to pull requests or issues.

If you have no ability to install python + required modules on server due to lack of Internet access, you may pull and save a docker image with all necessary for using modules on machine with Internet access and then copy/use the image on internal subnet without Internet.
Docker Hub image and instructions have provided here: https://hub.docker.com/repository/docker/dmitryzhdanov01/zabbixreport

Have a nice day :)
