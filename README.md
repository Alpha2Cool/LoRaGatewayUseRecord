## sx1301 gateway usage record

# 1. Log in to the gateway
The gateway ip is 172.0.41.196  
So modify the local ip to 172.0.41.xx  

# 2. Function disabled
Since the data receiving function on the web side  
and the command side cannot be enabled at the same time  
the receiving function on the web side should be disabled  
RUN:  
```
cd /risinghf/pktfwd  
sudo systemctl stop pktfwd  
```
To check the running status, execute the following command:  
`sudo systemctl status pktfwd`  
The status should be **inactive**  

# 3. Receive data
RUN:  
```
./pktfwd  
```
