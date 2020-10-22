# picoCTF – Irish-Name-Repo 3 

* **Category:** Web
* **Points:** 400

## Challenge

> Try to see if you can login as admin!

## Solution

Like other Irish Name repo challenges, this one also is allowing the debug. I fired a curl request to see how the SQL query is constructed at the backend.

```
curl "<URL>/login.php" -d "password=' OR 1=1 --&debug=1"

```
The response returned a query with 'OR' replaced. I realized that it's shift ciphered. After few trails, identified the key and replaced the characters based on it.

```
curl "<URL>/login.php" -d "password=' BE 1=1 --&debug=1"
```


```
picoCTF{3v3n_m0r3_SQL_xxxx}
```
