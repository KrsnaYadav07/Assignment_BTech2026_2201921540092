# Assignment_BTech2026_2201921540092
## Problem 1: Using inheritance, one class can acquire the properties of others. Consider the following Animal class:

## Platform Used : HackerRank

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
