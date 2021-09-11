# Chicago American Nazi Party

### We have to gain access to the administration page of the given website and post a message on the main page.

- URL : <https://www.hackthissite.org/missions/realistic/2/>

- So let's start by viewing the page source
- we can find a hidden link which is not visible directly to us as it is in black (which hides itself as the website bg color is also black) 
 ![hidden](hidden.png)
- this link leads us to a login page
- Now to get the administrator access we need the password, which will be saved in the database
- so to get unauthorised things from a database we can use SQLi(SQL injection)
- let's try `' OR 1=1 --` in the username field.
	- what this does is  
	```sql
		SELECT * FROM users WHERE username = ''	AND password = ''
		SELECT * FROM users WHERE username = '' OR 1=1 -- AND password = ''
	```
	we can see that the password check gets commented out (by the `--`)
- and we're in!