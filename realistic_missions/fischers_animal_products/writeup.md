# Fischer's Animal Products

### So in this mission we need to get the email list of the customers from the database

URL : <https://www.hackthissite.org/missions/realistic/4/>

- I entered a real email address and it gave no errors.
- then i tried giving a black email address, it threw an error stating the table we are storing the emails in, the `email`  table.
- now let's think of a sql injection.
- first we need to figure out the total number of existing tables in the database.
	- we can do this using the `ORDER BY` statement
	```sql
		https://www.hackthissite.org/missions/realistic/4/products.php?category=1 ORDER BY 1	
	```