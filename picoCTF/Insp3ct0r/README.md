# picoCTF – Insp3ct0r 

* **Category:** Web 
* **Points:** 50 

## Challenge

> Kishor Balan tipped us off that the following code may need inspection 

## Solution
Open the link provided next to the description. We need to inspect the source of the HTML. Prepend "view-source:" to the URL.

At the bottom of the source, 1/3 of the flag is visible. We need to find the other two missing pieces.

On closer look of the HTML, we can see CSS (mycss.css) and JS (myjs.js) file being refered with relative path. The second part of the flag is in the bottom of the CSS, and the last part of it is present in the JS file.

```
picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky*****}
```
