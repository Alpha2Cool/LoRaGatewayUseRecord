# SX1301 gateway usage record

## 1. Log in to the gateway
The gateway ip is 172.0.41.196  
So modify the local ip to 172.0.41.xx  

## 2. Change frequency plan
`cd /risinghf/pktfwd`  
The required frequency scheme can be changed by any of the following 4 commands:  
*CN470*  
`ln -sf global_conf_cn470.json global_conf.json`  
*CN433*  
`ln -sf global_conf_cn433.json global_conf.json`  
*AS920*  
`ln -sf global_conf_as920.json global_conf.json`  
*EU868*  
`ln -sf global_conf_eu868.json global_conf.json`  
![frequency plan table](https://github.com/Alpha2Cool/sx1301GatewayCmd/blob/master/fpt.PNG)  
After changing the frequency, you need to restart the Gateway service for the setting to take effect:  
`sudo /etc/init.d/lrgateway restart`  

## 3. Function disabled
Since the data receiving function on the web side  
and the command side cannot be enabled at the same time  
the receiving function on the web side should be disabled  
RUN:  
`cd /risinghf/pktfwd`  
`sudo systemctl stop pktfwd`  
To check the running status, execute the following command:  
`sudo systemctl status pktfwd`  
The status should be **inactive**  

## 4. Receive data
RUN:  
`./pktfwd`  

![gateway pic](https://github.com/Alpha2Cool/sx1301GatewayCmd/blob/master/gw.PNG)  
User Manual download address:  
[EN](https://alpha2cool.lanzous.com/il4TFmy5pvc)  
[CN](https://alpha2cool.lanzous.com/ihlZEmy5psj)  
