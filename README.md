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

## Exercise 4

```

INSERT INTO `invoices`
VALUES ('AUTO_INCREMENT','32','AX-014-027','8/1/2018','434.58','0','0','2','8/31/2018','null')

```
INSERTS a new record with an AUTO_INCREMENTED ID into the 'invoices' table
![Exercise 4 Screenshot](/assets/ch5-ex4.jpg)

## Exercise 5

```

INSERT INTO `invoice_line_items` 
VALUES ('115','1','160','128.23','Hard Drive'),
	   ('115','2','527','254.35','Exchange Server update')

```
INSERTS 2 Records into 'invoice_line_items' table
![Exercise 5 Screenshot](/assets/ch5-ex5.jpg)

## Exercise 6

```

UPDATE `invoices` SET credit_total=(.1*invoice_total), payment_total = (invoice_total-credit_total)
 WHERE invoice_id = 115

```
UPDATES's the last invoice record to have a credit total and a payment total
![Exercise 6 Screenshot](/assets/ch5-ex6.jpg)

## Exercise 7

```

UPDATE `vendors` SET default_account_number=403
WHERE vendor_id=44

```
UPDATES record with vendor id of 44 to have default account number of 403
![Exercise 7 Screenshot](/assets/ch5-ex7.jpg)

## Exercise 8

```

UPDATE invoices
INNER JOIN vendors ON invoices.vendor_id = vendors.vendor_id
SET terms_id = 2
WHERE vendors.default_terms_id = 2

```
JOINS the invoices vendor id with the vendor table and updates the invoice term id
![Exercise 8 Screenshot](/assets/ch5-ex8.jpg)

## Exercise 9

```

DELETE FROM invoice_line_items WHERE invoice_id = 115;
DELETE FROM `invoices` WHERE invoice_id = 115

```
DELETES invoice record added in exercise 4 and associated records with foreign key
![Exercise 9 Screenshot](/assets/ch5-ex9.jpg)
