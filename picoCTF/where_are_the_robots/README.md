# picoCTF – where are the robots

* **Category:** Web
* **Points:** 100

## Challenge

> Can you find the robots?

## Solution

The robots.txt file must be located at the root of a website. The robots exclusion instructs how the crawlers should crawl the specific website.

Append robots.txt to the website URL and open it. There is a Disallow entry for `/8028f.html` in it. Open that page, the flag is present in it.

```
picoCTF{ca1cu1at1ng_Mach1n3s_****}
```
