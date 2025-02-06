# Assignment_BTech2026_2201921540092
## Problem 1: Using inheritance, one class can acquire the properties of others. Consider the following Animal class:

## Platform Used : HackerRank
### Date: 25/01/25

class Animal{
    void walk(){
        System.out.println("I am walking");
    }
}
This class has only one method, walk. Next, we want to create a Bird class that also has a fly method. We do this using extends keyword:

class Bird extends Animal {
    void fly() {
        System.out.println("I am flying");
    }
}
Finally, we can create a Bird object that can both fly and walk.

public class Solution{
   public static void main(String[] args){

      Bird bird = new Bird();
      bird.walk();
      bird.fly();
   }
}
The above code will print:

I am walking
I am flying
This means that a Bird object has all the properties that an Animal object has, as well as some additional unique properties.

The code above is provided for you in your editor. You must add a sing method to the Bird class, then modify the main method accordingly so that the code prints the following lines:

I am walking
I am flying
I am singing

## Problem 2: A Java abstract class is a class that can't be instantiated. That means you cannot create new instances of an abstract class. It works as a base for subclasses. You should learn about Java Inheritance before attempting this challenge.

## Platform Used : HackerRank
### Date: 25/01/25

Following is an example of abstract class:

abstract class Book{
    String title;
    abstract void setTitle(String s);
    String getTitle(){
        return title;
    }
}
If you try to create an instance of this class like the following line you will get an error:

Book new_novel=new Book(); 
You have to create another class that extends the abstract class. Then you can create an instance of the new class.

Notice that setTitle method is abstract too and has no body. That means you must implement the body of that method in the child class.

In the editor, we have provided the abstract Book class and a Main class. In the Main class, we created an instance of a class called MyBook. Your task is to write just the MyBook class.

Your class mustn't be public.

Sample Input

A tale of two cities
Sample Output

The title is: A tale of two cities
## Problem 3: A Java interface can only contain method signatures and fields. The interface can be used to achieve polymorphism. In this problem, you will practice your knowledge on interfaces.
## Platform Used : HackerRank
### Date: 26/01/25

You are given an interface AdvancedArithmetic which contains a method signature int divisor_sum(int n). You need to write a class called MyCalculator which implements the interface.

divisorSum function just takes an integer as input and return the sum of all its divisors. For example divisors of 6 are 1, 2, 3 and 6, so divisor_sum should return 12. The value of n will be at most 1000.

Read the partially completed code in the editor and complete it. You just need to write the MyCalculator class only. Your class shouldn't be public.

Sample Input

6
Sample Output

I implemented: AdvancedArithmetic
12
Explanation

Divisors of 6 are 1,2,3 and 6. 1+2+3+6=12.
## Problem 4: Method Overriding: When a subclass inherits from a superclass, it also inherits its methods; however, it can also override the superclass methods (as well as declare and implement new ones). 

## Platform Used : HackerRank
### Date: 26/01/25

Consider the following Sports class:

class Sports{
    String getName(){
        return "Generic Sports";
    }
    void getNumberOfTeamMembers(){
        System.out.println( "Each team has n players in " + getName() );
    }
}
Next, we create a Soccer class that inherits from the Sports class. We can override the getName method and return a different, subclass-specific string:

class Soccer extends Sports{
    @Override
    String getName(){
        return "Soccer Class";
    }
}
Note: When overriding a method, you should precede it with the @Override annotation. The parameter(s) and return type of an overridden method must be exactly the same as those of the method inherited from the supertype.

Task
Complete the code in your editor by writing an overridden getNumberOfTeamMembers method that prints the same statement as the superclass' getNumberOfTeamMembers method, except that it replaces  with  (the number of players on a Soccer team).

Output Format

When executed, your completed code should print the following:

Generic Sports
Each team has n players in Generic Sports
Soccer Class
Each team has 11 players in Soccer Class

## Problem 5: When a method in a subclass overrides a method in superclass, it is still possible to call the overridden method using super keyword. If you write super.func() to call the function func(), it will call the method that was defined in the superclass.

## Platform Used: HackerRank
### Date:27/01/25

You are given a partially completed code in the editor. Modify the code so that the code prints the following text:

Hello I am a motorcycle, I am a cycle with an engine.
My ancestor is a cycle who is a vehicle with pedals.

## Problem 6: The Java instanceof operator is used to test if the object or instance is an instanceof the specified type.

## Platform Used: HackerRank
### Date: 27/01/25

In this problem we have given you three classes in the editor:

Student class
Rockstar class
Hacker class
In the main method, we populated an ArrayList with several instances of these classes. count method calculates how many instances of each type is present in the ArrayList. The code prints three integers, the number of instance of Student class, the number of instance of Rockstar class, the number of instance of Hacker class.

But some lines of the code are missing, and you have to fix it by modifying only  lines! Don't add, delete or modify any extra line.

To restore the original code in the editor, click on the top left icon in the editor and create a new buffer.

Sample Input

5
Student
Student
Rockstar
Student
Hacker
Sample Output

3 1 1

## Problem 7: Java Iterator class can help you to iterate through every element in a collection. Here is a simple example:

## Platform Used: HackerRank
### Date: 27/01/25

import java.util.*;
public class Example{

    public static void main(String []args){
        ArrayList mylist = new ArrayList();
        mylist.add("Hello");
        mylist.add("Java");
        mylist.add("4");
        Iterator it = mylist.iterator();
        while(it.hasNext()){
            Object element = it.next();
            System.out.println((String)element);
        }
    }
}
In this problem you need to complete a method func. The method takes an ArrayList as input. In that ArrayList there is one or more integer numbers, then there is a special string "###", after that there are one or more other strings.
A sample ArrayList may look like this:

element[0]=>42
element[1]=>10
element[2]=>"###"
element[3]=>"Hello"
element[4]=>"Java"
You have to modify the func method by editing at most 2 lines so that the code only prints the elements after the special string "###". For the sample above the output will be:

Hello
Java
Note: The stdin doesn't contain the string "###", it is added in the main method.

To restore the original code in the editor, click the top left icon on the editor and create a new buffer.
## Problem 8: Suppose you are designing a basic system to model different types of animals. There are two types of animals: Animal and Dog. Each animal has an attribute called name.
## Platform Used: CodeChef
### Date: 28/01/25

Create a base class Animal with a property name (a string).
Create a class Dog that inherits from Animal. The Dog class should have an additional property breed (a string) to represent the breed of the dog.
In the main function, create an instance of the Dog class, set its name and breed properties, and then display the name and breed of the dog.
Ensure that the base class Animal and the derived class Dog are correctly designed and that the properties are inherited and initialized properly.

Task
Given name and breed of dog as input, use display function to print the information of dog.

Input Format
First line contain the name of the dog.
Second line contain the breed of the dog.
Output Format
Print name of the dog on first line.
Print breed of the dog on second line.
Sample 1:
Input
Output
Buddy
Retriever
Buddy
Retriever

## Problem 9: Encapsulation and Accessors Usage
## Platform Used: CodeChef
### Date: 28/01/25

We know that members declared as private are only accessible from within the class itself. They are not accessible from outside the class, including derived classes (in the case of inheritance).
Thus here we will learn how to access and modify the private data of classes.
We are given a class User having name and password as private data. This class also contain two methods get and set which are used to access and modify private data.

Note - "this" is used within a class member function to refer to the object on which the member function is called. You can refer to the code to know how to use it.

Task
Initially the name of the user is "Alice" and password is "Wonderland". Print this information using get function.
Now, change the name of the user to "Tom" and password to "Jerry" using set function. Print this information using get function.
Run this code to verify the output.

## Program 10: Bank Account Class
## Platform Used: CodeChef

### Date: 29/01/25
This code demonstrates a basic implementation of a bank account system using object-oriented programming (OOP) principles in Java. Here's an explanation of the code:

BankAccount Class:

This class represents a bank account.
It has three private attributes: accountNumber, accountHolder and balance
The class includes a constructor to initialize the attributes when creating a new account.
Deposit Method (deposit): This method allows you to deposit a specified amount into the account.

Withdraw Method (withdraw): This method allows you to withdraw a specified amount from the account.

Get Account Information Method (getAccountInfo):

This method displays the account information, including the account number, account holder's name, and the current balance.
Task
Create an instance of the BankAccount class named account with an initial account number = 12345 and account holder's name = John Doe. Perform deposit of 1000, withdrawal of 500 and deposit of 200. Finally, display the account information using the getAccountInfo method.

This code simulates a simple bank account system where you can create an account, deposit and withdraw funds, and view the account details.

Sample 1:
Input
Output
 
Deposited: $1000
Withdrawn: $500
Deposited: $200
Account Number: 12345
Account Holder: John Doe
Balance: $700

## Problem 11: Eligibility Checker for Students
## Platform Used: CodeChef
### Date: 30/01/30
You are tasked with designing a simple program that determines the eligibility of students based on their scores and ages.

Class Definitions:

Student class:
Attributes:
name (String): The name of the student.
score (int): The student's academic score.
age (int): The age of the student.
Methods:
eligible(): A method that checks the student's eligibility and prints "YES" if the score is greater than 10 and the age is greater than 20. Otherwise, it prints "NO."
Main Class:

Codechef class:
The main method:
Creates an instance of the Student class.
Sets the name, score, and age attributes for the student with predefined values.
Calls the eligible method to determine and display the student's eligibility.

## Problem 12: Rectangle Class
## Platform Used: CodeChef
### Date: 30/01/30
Write a class Rectangle with length and breadth as attribute and area and perimeter as methods. Given length and breadth as input, Print area and perimeter of rectangle using area and perimeter methods respectively.

Input Format
The first line of input contains length of rectangle.
The second line of input contains breadth of rectangle.
Output Format
First line contains the output of area method of Rectangle.
Second line contains the output of perimeter method of Rectangle.
Sample 1:
Input:
2
3
Output:
6
10
## Program 13: How to deal with Private Data Member
## Platform Used: CodeChef
### Date: 31/01/25

In Java, getter and setter methods are used to access and modify private data members (fields) of a class. Here's how you can create getter and setter methods for private data members:

Getter Method: A getter method allows you to retrieve the value of a private field.

Setter Method: A setter method allows you to modify the value of a private field.

Using Getter and Setter: You can use the getter and setter methods to access and modify the private field.

In this example, the setMyField method sets the value of myField, and the getMyField method retrieves the value. Getter and setter methods provide controlled access to private fields.

## Problem 14: Ambiguity in Multiple inheritance.
## Platform Used: CodeChef
### Date: 31/01/25

Let's see the example by using two base classes and one derived class to demonstrate the multiple inheritance ambiguity, often referred to as the "diamond problem" in C++.

Suppose you have two base classes:

BaseA - The first base class with a method called foo().
BaseB - The second base class with a method called foo() as well.
Derived - Inherits from both BaseA and BaseB.
In this simplified example, when you call derived.foo() Line 24, the compiler doesn't know whether you want to call foo() from BaseA or BaseB because both base classes provide an implementation of foo(). This ambiguity is the essence of the diamond problem

## Problem 15: Design Parking System
## Platform Used: LeetCode

### Date: 01/02/25

Design a parking system for a parking lot. The parking lot has three kinds of parking spaces: big, medium, and small, with a fixed number of slots for each size.
Implement the ParkingSystem class:

ParkingSystem(int big, int medium, int small) Initializes object of the ParkingSystem class. The number of slots for each parking space are given as part of the constructor.
bool addCar(int carType) Checks whether there is a parking space of carType for the car that wants to get into the parking lot. carType can be of three kinds: big, medium, or small, which are represented by 1, 2, and 3 respectively. A car can only park in a parking space of its carType. If there is no space available, return false, else park the car in that size space and return true.
 

Example 1:

Input
["ParkingSystem", "addCar", "addCar", "addCar", "addCar"]
[[1, 1, 0], [1], [2], [3], [1]]
Output
[null, true, true, false, false]

Explanation
ParkingSystem parkingSystem = new ParkingSystem(1, 1, 0);
parkingSystem.addCar(1); // return true because there is 1 available slot for a big car
parkingSystem.addCar(2); // return true because there is 1 available slot for a medium car
parkingSystem.addCar(3); // return false because there is no available slot for a small car
parkingSystem.addCar(1); // return false because there is no available slot for a big car. It is already occupied.
 

Constraints:

0 <= big, medium, small <= 1000
carType is 1, 2, or 3
At most 1000 calls will be made to addCar

## Problem 16: Design an Ordered Stream
## Platform Used: LeetCode
### Date: 02/02/25

There is a stream of n (idKey, value) pairs arriving in an arbitrary order, where idKey is an integer between 1 and n and value is a string. No two pairs have the same id.

Design a stream that returns the values in increasing order of their IDs by returning a chunk (list) of values after each insertion. The concatenation of all the chunks should result in a list of the sorted values.

Implement the OrderedStream class:

OrderedStream(int n) Constructs the stream to take n values.
String[] insert(int idKey, String value) Inserts the pair (idKey, value) into the stream, then returns the largest possible chunk of currently inserted values that appear next in the order.
 

Example:
Input
["OrderedStream", "insert", "insert", "insert", "insert", "insert"]
[[5], [3, "ccccc"], [1, "aaaaa"], [2, "bbbbb"], [5, "eeeee"], [4, "ddddd"]]
Output
[null, [], ["aaaaa"], ["bbbbb", "ccccc"], [], ["ddddd", "eeeee"]]

Explanation
// Note that the values ordered by ID is ["aaaaa", "bbbbb", "ccccc", "ddddd", "eeeee"].
OrderedStream os = new OrderedStream(5);
os.insert(3, "ccccc"); // Inserts (3, "ccccc"), returns [].
os.insert(1, "aaaaa"); // Inserts (1, "aaaaa"), returns ["aaaaa"].
os.insert(2, "bbbbb"); // Inserts (2, "bbbbb"), returns ["bbbbb", "ccccc"].
os.insert(5, "eeeee"); // Inserts (5, "eeeee"), returns [].
os.insert(4, "ddddd"); // Inserts (4, "ddddd"), returns ["ddddd", "eeeee"].
// Concatentating all the chunks returned:
// [] + ["aaaaa"] + ["bbbbb", "ccccc"] + [] + ["ddddd", "eeeee"] = ["aaaaa", "bbbbb", "ccccc", "ddddd", "eeeee"]
// The resulting order is the same as the order above.
 

Constraints:

1 <= n <= 1000
1 <= id <= n
value.length == 5
value consists only of lowercase letters.
Each call to insert will have a unique id.
Exactly n calls will be made to insert.

## Problem 17: Number of Recent Calls
## Platform Used: LeetCode
### Date: 03/02/2025

You have a RecentCounter class which counts the number of recent requests within a certain time frame.

Implement the RecentCounter class:

RecentCounter() Initializes the counter with zero recent requests.
int ping(int t) Adds a new request at time t, where t represents some time in milliseconds, and returns the number of requests that has happened in the past 3000 milliseconds (including the new request). Specifically, return the number of requests that have happened in the inclusive range [t - 3000, t].
It is guaranteed that every call to ping uses a strictly larger value of t than the previous call.

 

Example 1:

Input
["RecentCounter", "ping", "ping", "ping", "ping"]
[[], [1], [100], [3001], [3002]]
Output
[null, 1, 2, 3, 3]

Explanation
RecentCounter recentCounter = new RecentCounter();
recentCounter.ping(1);     // requests = [1], range is [-2999,1], return 1
recentCounter.ping(100);   // requests = [1, 100], range is [-2900,100], return 2
recentCounter.ping(3001);  // requests = [1, 100, 3001], range is [1,3001], return 3
recentCounter.ping(3002);  // requests = [1, 100, 3001, 3002], range is [2,3002], return 3

## Problem 18: Banking System with User-Defined Exceptions
## Platform Used: CodeChef
### Date: 04/02/2025
You are tasked with designing a simple banking system.
Implement the following components using C++ classes and user-defined exceptions:

Create a BankAccount class to represent a bank account.
Each account should have the following attributes:
Account Number (an integer)
Account Holder Name (a string)
Balance (a floating-point value)
Additionally, include a method withdraw that allows an account holder to withdraw money.
If the withdrawal amount exceeds the account balance, throw a InsufficientFundsException with an appropriate error message.
Create a InsufficientFundsException class that is derived from std::exception.
This class should include a constructor that takes an error message as a parameter.
In the main function:
Create several BankAccount objects.
Deposit and withdraw money from these accounts.
Catch and handle the InsufficientFundsException when a withdrawal exceeds the account balance.

Constraints:

1 <= t <= 109
Each test case will call ping with strictly increasing values of t.
At most 104 calls will be made to ping.

## Problem 19: Handling Out-of-Range Integer
## Platform Used: CodeChef
### Date: 05/02/2025

Create a C++ program that reads an integer from the user and handles the case when the entered integer is outside a specified valid range. Implement the following components:

Declare two integer constants, MIN_VALUE and MAX_VALUE, representing the inclusive lower and upper bounds of the valid range. Set MIN_VALUE to -1000 and MAX_VALUE to 1000.
try block:
If the entered integer is less than MIN_VALUE or greater than MAX_VALUE, throw an exception of type std::out_of_range with an appropriate error message.
catch block:
Catch the std::out_of_range exception.
Display an error message indicating that the entered integer is out of the specified range.

## Problem 20: Area of Rectangle
## Platform Used: TECHGIG
### Date: 06/02/2025

Create two classes:
BaseClass
The Rectangle class should have two data fields-width and height of int types. The class should have display()method, to print the width and height of the rectangle separated by space.
DerivedClass 
The RectangleArea class is derived from Rectangle class, i.e., it is the sub-class of Rectangle class. The class should have read_input() method, to read the values of width and height of the rectangle. The RectangleArea class should also overload  the display() method to print the area (width*height) of the rectangle.

Input Format
The first and only line of input contains two space separated integers denoting the width and height of the rectangle.

Constraints
1 <= width,height <= 10^3

Output Format
The output should consist of exactly two lines: 
In the first line, print the width and height of the rectangle separated by space. 
In the second line, print the area of the rectangle.
Sample TestCase 1
Input
12 9
Output
12 9
108
