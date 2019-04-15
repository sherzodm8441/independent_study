Entry 3 

What I learned this week was mostly based off what I needed to know to make my Java game. Since my game needs a window for the user to play on, I figured that it would be best if I learned how to make a window show up on my computer before jumping into the backend of the game.

JFrame

JFrame is a class in in Java's graphical user interface toolkit called Swing. What this class does is, as the name implies, is that it creates a frame or as we call it - a window. 

JPanel

If you want things show up inside your JFrame window, the program requires you to use a JPanel. JPanel is also a Swing class, but it is in control of what goes inside the window (canvas). 

For example, if you wanted a button to show up in your window first you would have a to create an instance of the button class. Then add it to the instance of the JPanel class. And then add the instance of the JPanel class to the instance of the JFrame class. 

So much goes into making just a button appear in your window. There are easier ways of doing this, mainly by using graphics APIs or other development toolkits but it is better to start with the basics first before jumping into advanced programming. 

## My JFrame

My code: 
```
public Renderer(){

        JFrame window = new JFrame("This is the game renderer");
        window.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        window.setResizable(false);
        window.setSize(new Dimension(600,1000));

    }
```

The code above creates a window and specifies a few things about it.
```
 JFrame window = new JFrame("This is the game renderer");
```
This line of code creates an instance of the JFrame and the text inside the parenthesis is the title of the window. 
```
window.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
```
This line makes sure that when you prees the X at the corner of your window to exit out the program terminates. Otherwise, the program will keep running even after the window closes which is not something we want (usually).
```
window.setResizable(false);
window.setSize(new Dimension(600,1000));
```
These two line set the size of the window and make it unresizeable by the user. 

The window is still blank so I used the code below to add some elements.

```
        JTextArea text = new JTextArea("This is text");

        JPanel panel = new JPanel();
        JButton button  = new JButton("Click me");
        panel.add(button);
        panel.add(text);
        window.add(panel);
        button.addActionListener(new Action());
        window.setVisible(true);
```
The first three lines initialize a text area, JPanel and a button. 
```
.add()
```
The function above adds the object in the parenthesis to the object that comes before the . (dot) operator.

After the objects are added they will show up inside the window. Well at least that's what I thought would happen. I almost gave up on life because I could not get the things I added to show up. I was about to leave the country to go live on some remote deserted island before a quick google search stopped me. it turns out that the order of the lines of code matter. Since this class runs each line of code only once, it is a good practice to leave making the window visible as the last thing you do. The line of code below makes the window visible, before I had it as my second line of code. When I moved all the way to the bottom everything was visible. 
```
window.setVisible(true);
```
There is a `repaint()` function that updates the screen but that it more for animations, which I will be learning more about and using later. 

When you run the code the result is a window with a button and a text area as shown below.

![windowjpg.jpg](images/windowjpg.jpg) 




