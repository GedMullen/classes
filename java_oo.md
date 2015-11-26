# Week 11 & 12

1 . Last class - review.
<br>2 . Week 10 answers - [Careworker.java](https://gist.github.com/GedMullen/358fecd38c195b52a3e6)
[Doctor.java](https://gist.github.com/GedMullen/1555613e8b147820a486)
[Nurse.java](https://gist.github.com/GedMullen/56b3a3a514d4c0ee5951)
[Consultant.java](https://gist.github.com/GedMullen/01a0b6381c4cbd6d7ad1)
<br>3 . [Oracle Certified Associate Java 7 Programmer 1](http://education.oracle.com/pls/web_prod-plq-dad/db_pages.getpage?page_id=5001&get_params=p_exam_id:1Z0-803&p_org_id=&lang=) 
<br>4 . [OCA Java 7 Book](http://www.amazon.co.uk/OCA-Java-Programmer-Certification-Guide/dp/1617291048)
<br>5 . [Polymorphism Image](https://drive.google.com/file/d/0B-CFaefA1v4RaFFSeUpPbkpKVDQ/view?usp=docslist_api)
<br>6 . [Polymorphism Definition](http://whatis.techtarget.com/definition/polymorphism)
<br>7 . [Polymorphism Tutorial](https://docs.oracle.com/javase/tutorial/java/IandI/polymorphism.html)
<br>8 . [Red Dwarf Polymorph Episode] (http://reddwarf.wikia.com/wiki/RD:_Polymorph)
<br>9 . [draw.io] (https://www.draw.io/)
<br>10 . [UML Tutorial] (http://www.tutorialspoint.com/uml/index.htm)

##Exercises

1. Complete the overriding exercises from Week 10.
2. Create a project in Eclipse on Ygritte called "polymorphism" and complete the [Polymorphism Tutorial](https://docs.oracle.com/javase/tutorial/java/IandI/polymorphism.html).
3. Continue in your Eclipse overriding project and create 4 CareWorker references to a Nurse instance, a CareWorker instance, a Doctor instance and a Consultant instance. Call the getFullName method on each of the references. Is the output what you would expect?
4. Create a Hospital class that contains an ArrayList<CareWorker> field. Add a toString method to Hospital that iterates through the ArrayList calling the getSpeciality, getBedsideManner and getFullName methods on each reference in the list. Write code to test your class using the objects you created in exercise 3.
5. Create and Object reference to a Hospital instance. Call the toString method on the Object reference. Is the output what you would expect?
6. You can use the Eclipse Debugger to further your understanding of how the JVM calls polymorphic methods. Go to the Window menu option in Eclipse and choose Help Contents. Then choose Java Development User Guide -> Concepts -> Debugger and read the guide to the Java Debugger. Use breakpoints and the "step into" functionality to see which polymorphic methods are actually being called when you run your code.  



# Week 10

1 . Last class - review.
<br>2 . [Overriding](http://www.tutorialspoint.com/java/java_overriding.htm)
<br>3 . Week 9 solution:
```java
public class CareWorker {
	
	private String firstName;
	private String secondName;
	private String speciality;
	
	public CareWorker(String firstName, String secondName, String speciality){
		this.firstName = firstName;
		this.secondName = secondName;
		this.speciality = speciality;
	}
	
	protected String getSpeciality(){
		return speciality;
	}
	
	protected String getFullName(){
		return firstName + " " + secondName;
	}
	
	public static void main(String[] args) {

		CareWorker careWorker = new CareWorker("Jeff", "Mullen", "Brain Surgeon");
		System.out.println(careWorker.getFullName());
	}

}

public class Doctor extends CareWorker {

	public Doctor(String firstName, String secondName, String speciality){
		super(firstName, secondName, speciality);
	}
	
	
	public String getFullName(){
		return "Dr " + super.getFullName();
	}

	
	public static void main(String[] args) {
		Doctor doc = new Doctor("Joe", "Blogs", "Brains");
		System.out.println(doc.getFullName());
	}

}

public class Nurse extends CareWorker {
	
	public Nurse(String firstName, String secondName, String speciality){
		super(firstName, secondName, speciality);
	}
	
	public String getSpeciality(){
		
		return super.getSpeciality() + "  - Nurse";
	}
	
	public static void main(String[] args) {
		
		Nurse nurse = new Nurse("Jef", "Mullen", "Eyes");
		System.out.println(nurse.getFullName());
		System.out.println(nurse.getSpeciality());
				
	}

}
```

##Exercises

1. Create an "overriding" project in eclipse on Ygritte and work through the [Overriding Tutorial](http://www.tutorialspoint.com/java/java_overriding.htm)
2. With your knowledge of overriding in mind, enhance the CareWorker exercise in Week 9 by adding a method called getBedsideManner() that returns a string. The bedside manner for all care workers should be "polite" but in addtion to this the nurse should also be "caring" and the doctor should also be "informative". For example, calling the getBedsideManner() method on Doctor should result in the program outputting "polite and informative".
3. In the same way that the tutorial example creates a Dog instance with an Animal reference, create a Doctor instance with a CareWorker reference and call the getBedsideManner() method. Is the output what you would expect?
4. In the same way that the tutorial example creates a Dog instance with an Animal reference, create a Nurse instance with a CareWorker reference and call the getBedsideManner() method.
5. Add a set and get method to Nurse for a headNurse field that returns the name of the Nurse's manager. Write code to test your new methods.
6. Create a nurse instance with a CareWorker reference and try to call the getHeadNurse() method. What happens?
7. Create three separate Nurse instances with CareWorker references and call all public methods on the Nurse instance. 
8. Create a file on Ygritte called wk10.txt and use it to store the answers to the following [quiz](https://docs.google.com/document/d/10JWQFIO04yI4Wp7wNKoInG2_hsdTgSUZEXlzRmZs7eU/pub).
9. Create a subclass of Doctor called Consultant.
10. Add a field to Consultant called areaCovered and add an overloaded constructor so that Consultant can be instantiated with an areaCovered field (e.g. Fife).
11. Override the getFullName method so that it returns "Consultant John Smith" rather than "Dr John Smith". How does this effect your access modifiers?
12. Create a CareWorker reference to a Consultant instance. What methods are available to the reference?
13. Create a Doctor reference to a Consultant instance. What methods are available to the reference?
14. Create a Consultant reference to a Doctor instance. What happens?


# Week 9

1 . Last class - review.
<br>2 . Answers to last week's [questions](https://docs.google.com/document/d/11qFvmUdGBx51ADcc5VI1KyU0El6HjFJPs7LWdLD-Lio/edit?usp=sharing)
<br>3 . [Inheritance](http://www.tutorialspoint.com/java/java_inheritance.htm)
<br>4 . Java is on [codecademy](https://www.codecademy.com/courses/learn-java)

##Exercises

1. Create a "inheritance" project in eclipse on Ygritte and work through the [Java Inheritance Tutorial](http://www.tutorialspoint.com/java/java_inheritance.htm)
2. With your knowledge of encapsulation and inheritence in mind complete the following exercise: Create three classes - a superclass "CareWorker" and two subclasses "Doctor" and "Nurse". The superclass has 3 attributes - firstName, secondName and speciality. The subclasses both have a method called getFullName() that returns a String of the first and second name of the care worker. If the care worker is a Doctor then "Dr" must be prepended to the full name. When accessing the string containinng the speciality of the careworker the profession of the careworker should also be included e.g. "Eyes (Nurse)". Write code to test your implementation.   
3. Complete the Java course on [codecademy](https://www.codecademy.com/courses/learn-java)

# Week 8 - Thursday

1 . Last class - review.
<br>2 . [Chapter 3 Mindmap](https://drive.google.com/file/d/0B-CFaefA1v4RamVtWVdBZk5xTlU/view?usp=sharing)
<br>3 . [Controlling Access to Members of a Class](https://docs.oracle.com/javase/tutorial/java/javaOO/accesscontrol.html)

##Exercises

1. Complete Chapter 3 of [OOP Demystified](http://www.amazon.co.uk/OOP-Demystified-A-Self-teaching-Guide/dp/0072253630). 
2. Create a file in Ygritte called `ch3.txt` and use this to record your answers to these [questions](https://docs.google.com/document/d/11qFvmUdGBx51ADcc5VI1KyU0El6HjFJPs7LWdLD-Lio/edit?usp=sharing).
3. Continue with the exercises from Week 6.


# Week 8

1 . Last week - review.
<br>2 . [Java and OO Glossary](http://www.cs.kent.ac.uk/people/staff/djb/oop/glossary.html)
<br>3 . [OOP Chapter 2 Mindmap](https://drive.google.com/file/d/0B-CFaefA1v4RVjBRVlZJZ1o1aU0/view?usp=sharing)
<br>4 . Week 6 Exercise 5 - printOverdrawnTransations() method
```java
	public void printOverdrawnTransations() {
		System.out.println("Date\t\t", "Description\t\t", "Amount\t\t", "Balance\t\t\n");
		for (int i = 0; i < (transactions.size()); i++) {
			Transaction temp = transactions.get(i);

			if (temp.getBalance() < 0) {
				System.out.println(temp);
			}
		}
	}
```
<br>5 . Overloaded move() method (Week 6 Exercise 7)
```java
	public void move(double xDisp, double yDisp) {
		x += xDisp;
		y += yDisp;
	}

	public void move(String direction, double distance) {
		switch (direction) {
		case "north":
			x += distance;
			break;
		case "south":
			x -= distance;
			break;
		case "east":
			y -= distance;
			break;
		case "west":
			y += distance;
			break;
		default:
			System.out.println("Inccoret input");

		}
	}
```
<br>6 . Chapter 1 Answers: 
 1 C
 2 A
 3 D
 4 A
 5 B
 6 C
 7 C
 8 A
 9 D
 10 B


##Exercises

1. Complete Chapter 2 of [OOP Demystified](http://www.amazon.co.uk/OOP-Demystified-A-Self-teaching-Guide/dp/0072253630). 
2. Create a file in Ygritte called `ch2.txt` and use this to record your answers to these [questions](https://docs.google.com/document/d/119Eem95JeIItO3leLjR1IOsC9duDKdHzLq6ywG8DeJs/pub).
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
