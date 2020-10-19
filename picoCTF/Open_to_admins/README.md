# picoCTF – Open-to-admins

* **Category:** Web 
* **Points:** 200 

## Challenge

> This secure website allows users to access the flag only if they are **admin** and if the **time** is exactly 1400. 

## Solution

Add two cookie entries to the website. The first being `admin` with value `True` and the second one is `time` with `1400` as the value. Click on the **Flag** button to see the flag.


```
picoCTF{0p3n_t0_adm1n5_xxxxx}
```
