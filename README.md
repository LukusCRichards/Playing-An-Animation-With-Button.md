# Playing An Animation With Trigger or Key.md

This tutorial will teach you how to implement an animation into a script that plays it through either a press of a key or when entering a trigger in the game.

## Implementing the Animation Into the Script

Create a script with an applicable name and create a public Animator variable and name it appropriately, like **anim**. Next, type the name of your Animator variable in void start and write it occordingly: anim = GetComponent<Animator>();
 
 In the void Update, create an if statement and write it occordingly:
 
 if (Input.GetKeyDown (KeyCode.[preffered key]))
 {
    anim.Play([name of the animation]);
 }
 
 If you want the animation to play after something enters a trigger, create a new void statement and write this instead:
 
 void OnTriggerEnter(Collider collision)
 {
    if (collision.tag == "[Tag Name]")
    {
        anim.Play([name of animation])
    }
 }
