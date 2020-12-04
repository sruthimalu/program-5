# program 5
 (a) Create a table class.Fields are name and id 

CREATE TABLE class (`id` INT PRIMARY KEY AUTO_INCREMENT,
    `name` VARCHAR(50));


(b) Insert values into the table 

INSERT INTO class (`name`) VALUES ("ram"), ("ravi"), ("yamuna");

(c) Display the table 

SELECT * FROM class

(d) Apply commit, save point and rollback commands 

START TRANSACTION;

INSERT INTO class (`name`) VALUES ("rahul");

ROLLBACK; 

INSERT INTO class (`name`) VALUES ("rahul");

COMMIT;

START TRANSACTION;

SAVEPOINT hillspoint;

INSERT INTO class (`name`) VALUES ("heaven");

ROLLBACK TO hillspoint;

COMMIT;
