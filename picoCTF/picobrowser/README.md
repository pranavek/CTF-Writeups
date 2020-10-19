# picoCTF – picobrowser  

* **Category:** Web
* **Points:** 200

## Challenge

> This website can be rendered only by picobrowser, go and catch the flag! 

## Solution

A broswer user-agent is a string which helps the server understand what browser is being used. The browser will add user agent header in the requests. 

Solution based on Firefox browser:
1. Open the web developer window and click on the Networks tab to see the HTTP requests.
2. On the website, click on the Flag button. 
3. From the requests listed on the Networks tab select the request that was made due to the above invocation. 
4. Right click and select 'Edit and Resend'
5. Update the header named `User-Agent` to `picobrowser` and  click on the Send button.

The response contains the flag.

```
picoCTF{p1c0_s3cr3t_ag3nt_xxxxx}
```
