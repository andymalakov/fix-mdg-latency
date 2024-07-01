# fix-mdg-latency
Jupyter Notebook that computes latency statistics for Ember FIX Market Data Gateway.


## How to use

Capture FIX gateway output using TCPDUMP:
```sh
sudo tcpdump -i eth0 -w fix-traffic-on-port-10001.pcap "tcp port 10001"
```

Load resulting PCAP file into the notebook. It uses SCRAPY Python library for loading PCAP files which may be slow for large capture files, so please be patient.

The notebook captures and prints HDR histogram of two metrics:

L1: Data Connector to FIX Engine output
L2: Data Connector to TCP packet timestamp

![image](https://github.com/andymalakov/fix-mdg-latency/assets/1916494/6c335650-5eeb-4f13-b5ab-679805031061)
