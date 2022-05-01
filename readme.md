# POC order by and sorting algorithm in MySQL
Based on the article [What is the sorting algorithm behind ORDER BY query in MySQL?](https://www.pankajtanwar.in/blog/what-is-the-sorting-algorithm-behind-order-by-query-in-mysql)

## How to do the test
### Filesort
Excecute the follow query:
```sql
explain select * from animes order by id, title;
```
It should show **Using filesort** in **extra** column.

### Index sort
Excecute the follow query:
```sql
explain select id from animes order by id;
```
It should show **Using index** in **extra** column.
