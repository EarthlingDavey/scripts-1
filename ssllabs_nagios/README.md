ssllabs + Nagios
==============

The script is to 
* check SSL grade for list of domains


Installation


Prepare `/etc/ssl_domains.txt`

```
#crontab:
0 */4 * * *     root    /usr/local/bin/ssllabs-scan.check scan
```


```
#nagios nrpe:
command[check_ssllabs]=/usr/local/bin/ssllabs-scan.check check
```