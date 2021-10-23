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

### How to protect your database from SQL Injection

## Demo

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
