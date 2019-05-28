## ENTRY 8

This week was pretty much straight forward since I knew what I needed to work on. But it does not mean it did not come with its fair share of challenges.

The main thing that I worked on this week was adding collision detection to the objects in the game. I wanted for the game to be able to tell be when the ship and one of the obstacles was touching each other.

A while back I had come across a built in function that detects when two objects are touching each other `object.intersects()` and I knew that I would need to use that. I looked up a few tutorials on how to use it and after I had gotten the idea, I tried it with my code. And wala - it did not work. For some reason it kept giving me syntax error saying that it did not know what `object.intersects()` was. I even copied and pasted that chunk of code from the tutorials. And still the same problem. 

Then I noticed that they were using `Graphics` objects with that function. But I on the other hand was using one `Graphics` object and one `Image` object. That is what I suspected was the problem, but I am still not sure. However, after a few periods of thinking and thinking and thinking, I came up with a solution. 

I made a method that created a rectangle (Graphics object) using the coordinates if the image. And when using the `intersects()` function I called the rectangle method on the ship object and it worked flawlessly. 
```java
public void checkCollision(){
        for(int i = 0;i < arrayList.size();i++){
            temp = (Obstacle) arrayList.get(i);
            Rectangle temp1 = temp.getRectBounds().getBounds();
            if (temp1.intersects(spaceship.newRect())){
                System.out.println("collision");
                score++;
            }
        }
}
```

Then to make sure that I could make something with it, I made a half baked scoring system which I will change once I add the astronauts to the game. 

![collision_demo](images/collision_demo.mp4)

## TAKEAWAYS

**Make use of what you already know.** When I ran into the problem which prevented the `.intersects()` from working, I started to look for ways to make it work with an Image object. After I was not able to get a satisfactory answer, I used what I knew. I knew that the function worked with Graphics objects, so I decided to create a Graphics object at the same location as the Image object which solved my problem.  




