# Notes

## Running instance
chmod 400 ec2-replica.pem
ssh -i "udacity-exercise-ec2.pem" ec2-user@ec2-54-191-243-181.us-west-2.compute.amazonaws.com
sudo yum install mysq
mysql -u admin -P 3306 -p -h hw-database.c5sy1tda9lmd.us-west-2.rds.amazonaws.com udacity
SHOW TABLES;
CREATE TABLE Persons (Name varchar(255));
INSERT INTO Persons VALUES ('John Doe');
SELECT * from Persons;

## Running instance - replica
chmod 400 ec2-replica.pem
ssh -i "ec2-replica.pem" ec2-user@ec2-3-127-210-78.eu-central-1.compute.amazonaws.com
sudo yum install mysq
mysql -u admin -P 3306 -p -h database-1-read-replica.ccjtggyfrutl.eu-central-1.rds.amazonaws.com udacity