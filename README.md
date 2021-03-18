# LG02 gateway downlink usage record  
  
## 1. Log in  
The gateway ip is 10.130.1.1  
So modify the local ip to 10.130.1.xx  
  
## 2. Use *single_tx* to send  
`$ cd /usr/bin`  
`$ ./single_tx -h`  
```
Usage: single_tx           [-f frequence] <uint> (default:868500000) target frequency in Hz  
                           [-r] set as rx  
                           [-s spreadingFactor] <uint> (default: 7)  
                           [-b bandwidth] <uint> default: 125k  
                           [-c coderate] <uint> LoRa Coding Rate [1-4]  
                           [-w syncword] <uint> default: 52, 0x34  
                           [-i] send packet using inverted modulation polarity  
                           [-l] continue mode  
                           [-m message] <text> send this message from radio  
                           [-h] show this help and exit  
```
Transmit on freq 902.3Mhz:  
`./single_tx -f 902300000 -s 7 -b 125000 -m 123321     # try many times!!!`  
or  
`./single_tx -f 902300000 -s 7 -b 125000 -m 123321 -l  # continue mode, higher packet reception probability`  
  
