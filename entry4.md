## ENTRY 4 

Since my final project for Java will be a game with animations, I decided to learn more about animations and how to create them using Swing.

## ANIMATION

An animation usually usually requires a sprite. To get a sprite to show up in your window you need to create an instance of the `ImageIcon` object and point it to the image location. Then you call the `.getImage` function on the newly created instance to actually extract the image. If you want, then you can call the `.getScaledInstance` function to resize the image.  

```java
ImageIcon ii = new ImageIcon("src/star.png");
star = ii.getImage();
star = star.getScaledInstance(50,50,Image.SCALE_DEFAULT);
```
To get the image to actually appear in your canvas you need to draw it using the `Graphics.drawImage` method. This method takes in the image instance, x and y positions and the observer. 

```java 
g.drawImage(star, x, y, this);
Toolkit.getDefaultToolkit().sync();
```
I learned that it is a good habit to include the line above after drawing an image because that line makes sure that when the program runs on different OS's everything runs smoothly. 

Since an animation is an illusion of movement which is achieved by redrawing a sprite many times at different positions, all we need to do to animate our sprite is to change the x and y positions. And it will look something like this: 
```java
public void starUp(){
        x++;
        y++;
    }
 if (y < B_HEIGHT){
        starUp();
    }
```
For animation to work, we also need to add a timer so that the program knows how often to change the x and y positions and repaint the image. 

```java
timer = new Timer(DELAY, this);
timer.start();
```
The timer object takes in to parameters. First one is the delay and the second one is the action listener. The delay parameter specifies how long to wait before repainting the image in milliseconds. (The ideal delay time is 16.7 milliseconds because that causes the program to repaint the image 60 times creating 60 frames per second, which is the number of times most monitors refresh their pixels per second). The second parameter points to the chunk of code that is supposed to run when the delay time is up. In this case, the second parameter is the method that changes the image position.  

![star_gif](images/star_gif.gif)

Another programming trick I learned was that when working with animations (or swing in general), it is better to have to have class that extends JFrame and another that extends JPanel. In my last entry, I talked about how after an object was created it would have to be added to JPanel and then that JPanel to JFrame. Having different classes for JPanel and JFrame eliminate the need for that. In addition, it helps save time and not repeat yourself (DRY).

## TAKEAWAYS

Consistency is key to learning something new. I took a break from independent study because of the spring break and when I returned I realized that I had forgotten some of the code I had written myself. As a result, I wasted time trying to figure out what my code was supposed to do. In other words, take a break but keep it short.  

