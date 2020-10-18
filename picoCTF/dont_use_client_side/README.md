# picoCTF – dont-use-client-side 

* **Category:** Web
* **Points:** 100

## Challenge

> Can you break into this super secure portal?

## Solution

Open the webiste and check the source of it. The login form has a submit button, which is invoking a JS method named `verify()`. This method is reading the password which user entered and checks if it's substring matches certain strings.  

```
	if (checkpass.substring(0, split) == 'pico') {
	 if (checkpass.substring(split, split*2) == 'CTF{') {
          if (checkpass.substring(split*4, split*5) == 'ts_p') {
           if (checkpass.substring(split*3, split*4) == 'lien') {
            if (checkpass.substring(split*5, split*6) == 'lz_7') {
             if (checkpass.substring(split*2, split*3) == 'no_c') {
```

Make use of the index used in the substring to find the password string. 

```
picoCTF{no_clients_plz_xxxxx}
```
