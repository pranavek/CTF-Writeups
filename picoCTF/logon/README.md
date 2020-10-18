# picoCTF – logon

* **Category:** Web
* **Points:** 100

## Challenge

> The factory is hiding things from all of its users. Can you login as logon and find what they've been looking at?

## Solution

Open the website. Login with any username and password. Check the cookies of this website. There is a cookie entry named 'admin', which has value set as False. Change the value to True and refresh.

```
picoCTF{th3_c0nsp1r4cy_l1v3s_******}
```
