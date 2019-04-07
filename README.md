# wana

A shell analyzer for web logs.

## Usage

./wana -FILTER_NAME1 FILTER_VALUE1 -FILTER_NAME2 FILTER_VALUE2 -COMMAND_NAME logfile1 logfile2 logfile3..

You can specify 4 filters, each type of filter 0..1 times.  
You can specify 0..1 commands.  
You can specify 0 files (proceeds to load logs from stdin) or >=1 files (proceeds to load logs or .gz archives with logs).  

## Filters
* -a YYYY-MM-DD hh:mm:ss	- show logs after date
* -b YYYY-MM-DD hh:mm:ss	- show logs before date
* -uri REGEX				- show logs with uri that matches entered regex
* -ip	IP					- show logs with ip that matches entered ipv4/ipv6

compatible date formats:  
YYYY-MM-DD  
YYYY-MM-DD hh  
YYYY-MM-DD hh:mm  
YYYY-MM-DD hh:mm:ss  

## Commands
* list-uri	- list of URIs that were called
* list-ip		- list of all IPs that called the server
* list-host	- list of hosts for each IP- if host not available, then prints the original IP
* hist-load	- histogram based on number of accesses each hour
* hist-ip		- histogram based on number of accesses for each IP

## Deployment

No installation required, just copy the script to a folder with logs and it will work.

## Tested on:

* ElementaryOS 5.0
* CentOS 7.6.1810
* FreeBSD 11.2


## Author

* [Tomáš Kender](https://github.com/tomaskender)
