# picoCTF – picobrowser  

* **Category:** Web
* **Points:** 200

## Challenge

> This website can be rendered only by picobrowser, go and catch the flag! 

## Solution

A broswer user-agent is a string which helps the server understand what browser is being used. The browser will add user agent header in the requests. 

Make a curl request to the flag endpoint with user-agent header set to `picobrowser`

curl "<URL>/flag" -H "User-Agent:picobrowser"

The response contains the flag.

```
picoCTF{p1c0_s3cr3t_ag3nt_xxxxx}
```
