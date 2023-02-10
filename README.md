# dba120-exam1
 Exam 1 for DBA 120

## Exercise 1
 ```
 INSERT INTO `terms`(`terms_id`, `terms_description`, `terms_due_days`) 
 VALUES ('6','Net due 120 days','120]')

 ```
 Adds new record into 'terms' table
![Exercise 1 Screenshot](/assets/ch5-ex1.jpg)


## Exercise 2

```
UPDATE `terms` SET `terms_description`='Net due 125 days',`terms_due_days`='125' 
WHERE terms_id = 6

```
Updates previously added record in 'terms' table
![Exercise 2 Screenshot](/assets/ch5-ex2.jpg)


## Exercise 3

```

DELETE FROM `terms`
WHERE terms_id = 6

```
Deletes previously updated record in 'terms' table
![Exercise 3 Screenshot](/assets/ch5-ex3.jpg)



