# argo-probes

## Web API 

This is a probe for checking AR and status reports are properly working. 
It checks if there are available AR and status data for a selected day. 

The usage of the script is:
```sh
$ usage: api.py [-h] -H HOSTNAME -tenant TENANT -rtype RTYPE -token TOKEN
              [-day DAY] [-t TIMEOUT] [-d DEBUG]
```

where:

 - (-H): the hostname of the web api 
 - (-tenant): the tenant name (ex. EGI)
 - (-rtype): the report type (ar or status)
 - (-token): the authorization token
 - (-day): the day to check (1,2 ..3 means 1 or 2 or 3 days back)
 - (-t): the timeout
 - (-d): prints some debug data when is set to on  (by default off)
 
### Usage example

```sh
$ ./web-api.py -H web-api.test.com -tenant tenantname -rtype ar -token 12321312313123 -day 1 -t 180 
```
