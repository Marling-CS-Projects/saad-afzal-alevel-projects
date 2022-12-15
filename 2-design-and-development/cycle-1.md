# 2.2.1 Cycle 1 - Initial set up&#x20;

## Design

### Objectives

In this cycle, I aim to create a really basic layout for my game using Kaboom.js. I will make a shape correspond to inputs made by the keyboard.

* [x] Set up Kaboom.js
* [x] Make a platform&#x20;
* [x] Make a character &#x20;
* [x] Make the character move with keyboard input



### Usability Features

Keyboard Input - The keyboard inputs will be a simple left and right, so as to just provide movement for now. It is also easy to remember the controls and what they do.

### Key Variables

| Variable Name | Use                                                                |
| ------------- | ------------------------------------------------------------------ |
| speed         | Speed of how fast the player moves the character                   |
| Space         | Allows the player to jump and have more control of their character |
| Left/Right    | Well allows the player to move left and right                      |

### Pseudocode

```
procedure spawn player (1,10)

Speed = 200

Presskey('a')
 playermove left with fixed speed
 playerflip is true
 
Presskey('d')
 playermove right with fixed speed
 playerflip is false 

Presskey('space')
  if playergrounded
  then playerjump 750


    
end procedure
```

## Development

### Outcome

The player now has the ability to move left and right on a platform, the player moves at a fixed speed.

### Challenges

One challenge I had was making the player jump successfully.Whenever i would press the space bar it would say that Player.Grounded is not a function. ive tested the same code on another Kaboom.js and it worked.

## Testing

Evidence for testing

### Tests

| Test | Instructions    | What I expect                | What actually happens            | Pass/Fail |
| ---- | --------------- | ---------------------------- | -------------------------------- | --------- |
| 1    | Pressed space   | Player jumps                 | Game stops working               | Fail      |
| 2    | Run code        | Player spawns succesfully    | Player spawned successfully      | Pass      |
| 3    | Pressed A and D | Player moves left and right  | Player has moved left and right  | Pass      |

### Evidence

![Character on platform ](<../.gitbook/assets/image (2).png>)

{% tabs %}
{% tab title="First Tab" %}
```
 const SPEED = 200

  keyDown("a", () => {
    Player.move(-SPEED , 0)
    Player.flipX(true);
  });

  keyDown("d", () => {
    Player.move(SPEED , 0)
   Player.flipX(false);
  });
  
  
  keyPress("space", () => {
     if (Player.grounded()){
     Player.jump(750)
  }


```
{% endtab %}
{% endtabs %}
