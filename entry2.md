## ENTRY 2

 This week I learned about two big topics in Java programming: Inheritence and Collections.

## INHERITENCE 

 Inheritence allows classes to inherit traits from other classes. Similar to how a child inherits traits from its parents. Intuatively, the class that passes on its traits is called the parent class and the class that inherits them is called the child class (think web development). The only difference is that instead of using "inherits" you use "extends." 

 Ex.
 ```
 public class iMacTwo extends iMacOne {
     //code goes here
 }
 
 ```
 The word after the class is the child class and the word after the "extends" is the parent class. Extending a class enables the child class to call all the methods in the parent class without redeclaring them in the child class. Sometimes you want to extend a class but you don't want to use all the methods in it or you want to use a method in a different way. And that is where polymorphism comes in. Polymorphism allows you to override a method that is on the parent class by redefining it in the child class.
 
 Even after overriding a method, sometimes you might need to use the original method. Clevver developers at Oracle have thought of that and created the keyword "super." When you use super followed by the name of the overridden method, it will ignore the method in the child class and calls it using the code in the parent class.
 
 ```
 super.someMethod(someArgument);
 ```
 
 There is a limitation with parent/child classes and it is that a child class can only inherit from one parent class. To solve this the developers have added something called an "interface." 
 
 Creating an interface:
 ```
 public interface interfaceName{
     //code goes here
 }
 ```
 An interface is not like a class meaning that you cannot instentiate it. Its only purpose is to be implemented by other classes. A class can implement many interfaces at once and that solves the parent/child limitation. 
 
 Implementing an interface:
 ```
 public class someClass implements InterfaceOne, InterfaceTwo{
     //code goes here
 }
 ```
 An interface only declares methods but the code that tells the method what to do is written in the child class.
 
 If you don't want a class to be overridden, you can declare your method with with the keyword "final." This keyword makes sure that if a class inherits from it cannot override the specified method.
 
 Using final in a method:
 ```
 public final boolean thisIsAMethod(){
     //code goes here
 }
 ```
 
 Final keyword can also be used on variables (fields). When you use it on a variable, they no longer behave like a variable meaning that you cannot change the value of that variable (oxymoron?).
 
 Using final on a field:
 ```
 public final long number =  656519816898465135968435168;
 ```
 
 And that is pretty much it for inheritence.
 
 ## COLLECTIONS
 
 When I was doing the "Intro to Java" in Udacity, it was very discouraging to learn that arrays are not resizeable in Java. This means that when you want to use an array in Java, first you have to initialize it with the number of cells you want it to have and once that number is set you cannot change. So if you wanted to make your array bigger, you would have a create another array and gives it a cell number that bigger than the one in the array you want to expand and then copy the elements from the smaller array (using loops) and then delete the smaller array. As you can imagine this is a hassle.
 
 ![capture.jpg](https://digitalsynopsis.com/wp-content/uploads/2015/03/web-designer-developer-jokes-humour-funny-30.jpg)
 
 Thankfully all of my worries went away once I learned that Collections were there to make my worries go away. 
 
 Java Collections, as the name implies, is a collection of classes, interfaces and methods that are meant to make programming in Java easier and less of a hassle.
 
 The problem mentioned above can be solved with a class called ArrayList. When you initialize an array using ArrayList there is no need to specify the length of the array. Or when you want to add an element to the array, you simply add it using the keyword - add. Or if you want to remove an element you use the keyword "remove." The class ArrayList takes care of the resizing for you. An ArrayList basically acts like a wrapper for arrays.
 
 Creating an instance of ArrayList:
 ```
 ArrayList arrayList = new ArrayList();
 
 arrayList.add("item"); //adds items to the array
 arrayList.add("item1");
 
 arrayList.remove(0); //removes the first item from the array
 ```
 
 ArrayList is only one the many useful classes in the Collections framework. And I cannot talk about all of them here because there are so many.
 
 ## TAKEAWAYS 

 1. Don't jump to conclusions and get your hopes down. I was genuinely saddened when I found out that arrays in Java had so many annoying limitations (because is a program even a program without a bunch of arrays). But learning more about the language made me realize that others too are annoyed by the limitations (not just with arrays) and have created workarounds and shortcuts to address the problem.
 
## GOAL FOR NEXT WEEK

 I will start building my app by next week because at this point I am not even sure what I need to learn this make my app. So I figured that the best way for me to learn would be to start making the app and running into problems and learn by fixing those problems.   
 
 
 