# Automation-Project---PL-SQL-

ALL TABLES CREATED AND INSERTED WITH VALUES IN "tables_created.txt" .

itmmast table is the item master table and stores information about the products available.

cstmast table is the cvustomer master table and stores information related to the customer/user if any.

trn table is a transaction table which stores all the transactions taking place involving the given products.

The following validations must be done before inserting data into the trn table:

i) Make sure that the quantity required by the users is available by checking the itmmast table. If the quantity exists then the price of the item must be made available. If it does not exist price must be set to zero which implicates that there is no stock.

ii) Using the price of the item calculate the amount of sale (quantity * price) and check the cstmast table to see if the customer has adequate deposit to cover the amount of sale .

iii) If both validations are successful the data must be inserted into the trn table and the follwing updations must be done:
    a)Reduce the stock by quantity in the itmmast table
    b)Reduce the customer deposit by the sale value in the cstmast table


Solution:

A trigger is written for the trn table . The trigger will call a function and a procedure to perform the required validations. Therefore, 3 files are created for the trigger(trigger.txt), function(function.txt) and procedure(procedure.txt).

