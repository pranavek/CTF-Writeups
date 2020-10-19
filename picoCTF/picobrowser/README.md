# picoCTF – picobrowser  

* **Category:** Web
* **Points:** 200

## Challenge

> This website can be rendered only by picobrowser, go and catch the flag! 

## Solution

A broswer user-agent is a string which helps the server understand what browser is being used. The browser will add user agent header in the requests. 

The header can be modified in multiple ways;
1. From the dev console of the browser 
2. Using a proxy to intercept the request and modify the header
3. Using a broswer plugin
4. Overrding the agent using browser confi editor eg: about:config

The approach #1 is not working on Firefox as the newly added user-agent is getting overriden by it before making the request. 

I'm using the 4th approach. On Firefox browser, open `about:config` and add new String key named `general.useragent.override` with value `picobrowser`. Click on the Flag button.

```
picoCTF{p1c0_s3cr3t_ag3nt_xxxxx}
```
