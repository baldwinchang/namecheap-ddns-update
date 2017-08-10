## Attribution Notice

This repository and image is a direct fork of [joshuamorris3/namecheap-ddns-update](https://github.com/joshuamorris3/namecheap-ddns-update)

# namecheap-ddns-update
Update the IP address of your [namecheap.com](http://namecheap.com) Dynamic DNS A records.

## Overview
Use this to update the IP address of A records for a domain that is hosted by [namecheap.com](http://namecheap.com). If you created one or more A records using [namecheap.com](http://namecheap.com) Dynamic DNS, then this will update the IP address to:
* The IP address you pass in as an argument using -i
* Or, if the -i is omitted or left blank, the IP address seen by [namecheap.com](http://namecheap.com)'s servers when you run this script. If you run this from within your network, then the externally visible IP address is used by [namecheap.com](http://namecheap.com) to update the A record value. If you have a server with a public IP address, then this utility can be run from that server and -i can be omitted.


### Docker
You can also run this by pulling it from the Docker Hub.

```
docker pull baldwinchang/namecheap-ddns-update
```

Run the image you just built, passing in the environment variables to configure the script
```
docker run -e "NC_DDNS_PASS=123456" -e "DOMAIN=example.com" -e "SUBDOMAIN=abc" -e "INTERVAL=10s" -d baldwinchang/namecheap-ddns-update
```
