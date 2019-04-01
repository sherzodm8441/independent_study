## ENTRY 1

Even before we started the exploration week I had my mind set on Java. The first time that I ever heard about Java was when I was in middle school when I was forming interest in computer programming. I saw many videos of people making applications using Java, but since I did not know a thing about programming those tutorials made no sense to me. For the next eight weeks, I want to amke it a challenge for myself to learn Java and make an application using it. 

## WHAT IS JAVA?

Java is an object-oriented computer programming language that can be used to make cloud based applications, web APIs, client applications and etc. Java programs run on a Java Virtual Machine (JVM), which means that one version of the code can run on different operating systems. This eliminates the need for writing the same application using a different programming language for a certain operating system. Java is also used for programming Android applications using Android Studio.

## APP IDEA    

For my application I want to recreate the space ship game I made using p5js. When I made the game I also wanted to port it to my android phone. Since Android uses Java, I was not able to. So my goal is to make that game again using Java. If I can get the MVP to work early, I want to try to port it to my android device. In addition to knowing Java, I will also need to know how to use Swing as it is used to create graphical user interface. 

So my game has three main objects: the spaceship, obstacles and the astronauts. The spaceship only moves on the x-axis. On the p5js version, the user presses the left arrow once to make the spaceship move left and presses the right arrow key to make it go right. The obstacles stick out from both sides of the screen and only leave a little bit of space in the center for the spaceship to go through. The challenge is to keep the spaceship in the center to that it does not hit the obstacles. The astrnouts are scattered all aorund the screen and user must try to rescue them while avoiding the obstacles. 

## LEARNING JAVA

There is this website called udacity.com, which offers many programming languages for free including Java. Their java course has two parts "Intro to Java" and "Object-Oriented Programming in Java". I had finished the first part in the past, so this week I picked up from part two. After a couple of guided projects, meaning that they provided the code for the rpoject if I felt stuck, I was almost able to finish an unguided one. The name of this project is GuessTheMovie (Java used camelCase), in which the program picks out a movie title from a .txt file and displays the underscores to represent the number of characters there are in the title. The user enters a letter and the program sees is the letter inputted is part of the title, if it is then it replaces the underscore that was substituted for that letter with that letter. 

For example, the word "Inception" has nine letters so the underscores would look like this "_________". If the user entered the letter "e", then the underscores would look like this "___e____".

I almost got it to work except for that it if there is a duplicate of a letter it only replaces one of them. I think I know where the problem lies and I will get to fixing it once I finish this entry. 

Below is the code for the project (sorry about the code looking weird):

```import java.io.File;
import java.util.Scanner;


public class GuessTheMovie {
    public static void main(String [] args) throws Exception{
        File file = new File("movie");
        Scanner scanner  = new Scanner(file);

        String movie = scanner.nextLine();
//        System.out.println(line.length());
        String movieUnderScore = "";
        String underScore = "_";
```
        for(int i=0;i<movie.length();i++){

```
            movieUnderScore += underScore;
        }
        System.out.println(movieUnderScore);
        System.out.println("The movie has " + movie.length() + " characters. Now enter a letter");
//        System.out.println(movie.indexOf("r",3));

        while (movieUnderScore.contains(underScore)){
            Scanner userScanner = new Scanner(System.in);
            String userInput = userScanner.next();
//        System.out.println(userInput);
//        System.out.println(movie.indexOf(userInput));
            if(movie.contains(userInput)){
                String [] arr = movieUnderScore.split("");
                arr[movie.indexOf(userInput)] = userInput;
                movieUnderScore = String.join("",arr);
                System.out.println(movieUnderScore);

            }
            else{
                System.out.println("sorry this letter is not in the movie name");
            }
        }
    }
}
```
## TAKEAWAYS

A rule that I learned which could save a lot of time is that before writing a function, google if there is an already built in function that does the same thing. One of the things that my code needed to do was that it needed to see if a letter entered by the user was in the movie title. I was about to whip out my notes on Java loopd and make a function that would  do such that. Then I learned that Java has this built in function called .contains() which returns a true or false. This function saved me from hours of work. So did the funstion .indexOf(), which checks for the index of a specific letter in a string and returns it. I used that function to make the substitution. 

## GOAL FOR NEXT WEEK

My goal for next week is to focus more on classes so I could really make use of the power of Object oriented programming.








