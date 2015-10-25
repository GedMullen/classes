# Week 8

1 . Last week - review.
<br>2 . [Java and OO Glossary](http://www.cs.kent.ac.uk/people/staff/djb/oop/glossary.html)
<br>3 . [OOP Chapter 2 Mindmap](https://drive.google.com/file/d/0B-CFaefA1v4RVjBRVlZJZ1o1aU0/view?usp=sharing)
<img src="https://drive.google.com/file/d/0B-CFaefA1v4RVjBRVlZJZ1o1aU0/view?usp=sharing" height="100" width="100">

##Exercises

1. Complete Chapter 2 of [OOP Demystified](http://www.amazon.co.uk/OOP-Demystified-A-Self-teaching-Guide/dp/0072253630). 
2. Create a file in Ygritte called `ch2.txt` and use this to record your answers to these [questions](https://docs.google.com/document/d/10kjRuck14f6pJbvaaRL0jLuZb_IYrAVMeZ5-EfsiwzI/pub).
3. Continue with the exercises from Week 6.


# Week 7

1 . Last week - review.
<br>2 . The Transaction class:
```java
import java.text.SimpleDateFormat;
import java.util.Date;

public class Transaction {
        private double amount;
        private String date;
        private String description;
        private double balance;

        public Transaction(double amount, String description, double balance) {
                this.amount = amount;
                this.date = setDate();
                this.description = description;
                this.balance = balance;
        }

        public String setDate() {
                SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd:HH-mm-ss");
                return sdf.format(System.currentTimeMillis());
        }

        public String toString() {
                return date + "\t" + description + "\t" + amount + "\t" + balance;
        }
}
```
3 . Instantiating an ArrayList of Transaction objects in Account.java:
```java
private ArrayList<Transaction> transactions = new ArrayList<Transaction>();
```
4 . [UML Distilled](http://www.amazon.co.uk/UML-Distilled-Standard-Modeling-Technology/dp/0321193687)
<br>5 . [OOP Demystified](http://www.amazon.co.uk/OOP-Demystified-A-Self-teaching-Guide/dp/0072253630)

##Exercises

1. Complete Chapter 1 of [OOP Demystified](http://www.amazon.co.uk/OOP-Demystified-A-Self-teaching-Guide/dp/0072253630). 
2. Create a file in Ygritte called `ch1.txt` and use this to record your answers to these [questions](https://docs.google.com/document/d/10kjRuck14f6pJbvaaRL0jLuZb_IYrAVMeZ5-EfsiwzI/pub).
2. Continue with the exercises from Week 6.
3. Create a shell script called `checkoopbasics.sh` in the bin directory of your OOPBasics project and use it to run all your test code for the exercises completed within this project. Add to the shell script as you complete your exercises. Remember to make the script executable by issueing the following command:

`chmod 700 checkoopbasics.sh`




# Week 6

1. Last week - review.
2. [OOP Basics](https://www3.ntu.edu.sg/home/ehchua/programming/java/J3a_OOPBasics.html)
3. [Java ArrayList](http://www.tutorialspoint.com/java/java_arraylist_class.htm)
4. [Java Arrays](http://www.tutorialspoint.com/java/java_arrays.htm)
5. [Java Dates And Times](http://www.tutorialspoint.com/java/java_date_time.htm)

##Exercises

1. Complete Week 5 Exercises
2. Create a new project in Eclipse on Ygritte called OOPBasics and complete the [OOP Basics](https://www3.ntu.edu.sg/home/ehchua/programming/java/J3a_OOPBasics.html) tutorial. Create the classes in this tutorial as instructed.
3. You have been tasked with modifying the Account class in Example 3.1 in the tutorial above to include a record of transactions associated with the account. An extra method called printStatement() needs to be added to the class so that a statement of transactions can be issued as required. The method should list the date, description and amount of the transaction with an updated balance amount. Hint: you will need to modify the implementation of the credit() and debit() methods and store your transaction history in an Array or an ArrayList. The date of the transaction should be derived (i.e. set it to current time) and not passed as a parameter. Modify the TestAccount class to test the modified code. Create at least 10 transactions with a mixture of credit and debit.
4. Modify the Account class to allow customers to withdraw funds even if they do not have a positive balance. Create a method called hasBeenOverdrawn() that returns a value of true if the account has been overdrawn at any time. Create appropriate test code. 
5. Create another method in the account class called printOverdrawnTransactions() that prints all the transactions that are associate with the Account that have resulted in a negative balance. Create appropriate test code.
6. Create a shell script called checkoopbasics.sh in the bin folder of your OOPBasics project and add an entry into the script that runs your test code for exercises 3-5. Add entries into this shell script as you complete the exercies below. 
7. Create an overloaded move() method in the ball class in section 3.2 that takes a direction string of the value "north","south","east" or "west" and a distance attribute and moves the ball in the required direction the required distance. Create appropriate test code.
8. You have been asked to redesign the UML diagram in 3.3. Your modified design should change the Author class to have an array of Books as a field of the Author class. Use appropriate accessor methods. Remove the Author attribute from the Book class. Create appropriate test code.
9. Add a printBooks() method to the Author class that will print a description of the books published by the author. Create appropriate test code.
10. Add a printBooksOutOfStock() method to the Author class.
11. Add a getMostExpensiveBook() method to the Author class.
12. Redesign the Student class in section 3.4 so that the courses and grades array fields are encapsulated by a separate class called Unit. The Student class will then contain a Unit array field. Add two additional fields to the Unit class - attendance and effort. Like the grade field the attendance and effort fields should be in the range 0-100. Add the accessor methods for these new fields.
13. Add a constant class field called PASS_MARK to the Unit class and set it to 60.
14. Create a isPassed() method to the Unit class that averages the grade, attendance and effort fields and then compares the average to PASS_MARK and returns the value of true or false.  

# Week 5

1. Last week - review.
2. Tutorials
  * [Objects and Classes](http://www.tutorialspoint.com/java/java_object_classes.htm)
  * [Variable Types](http://www.tutorialspoint.com/java/java_variable_types.htm)
  * [Modifier Types](http://www.tutorialspoint.com/java/java_modifier_types.htm)

##Exercises

1. Complete Week 2 & 4 Exercises
2. Create a shell script called checkwarmup.sh to test that your week 2 and 4 exercises work correctly. Create the shell script in the same folder as your class files and run your classes using the following commamd:

 `java -cp . Wk4Ex1` 

3. Complete the tutorials above.
4. ~~Create a new project called OOPExercises in Eclipse on Ygritte and start work through these [Java OOP Exercises](https://www3.ntu.edu.sg/home/ehchua/programming/java/J3f_OOPExercises.html). Make sure you create the classes in your Eclipse project as directed by the instructions in the exercises.~~
