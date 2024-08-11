# Challenge - Events

## Events

Turtle allows us to detect when the user has hit certain keys on the keyboard or clicked the mouse. Whenever the user does one of these action it is called an event. We can listen for events and trigger functions to run if we "hear" the event.

### On click

If you wanted something to happen when the mouse is clicked you can use the `onclick` function. `onclick` takes a function that will be called when the click happens. This function has to take two inputs which are the co-ordinates of the click. For example:

```
import turtle as t

# Get the screen
screen = t.getscreen()

# Define function to put the pen down and move the turtle
def move(x, y):
    t.pendown()
    t.goto(x, y)

# Call the move function when the screen is clicked
screen.onclick(move)
```

This will call the function `move` whenever the screen is clicked. This is because the function is called on `screen` (the syntax is `screen.`). If you wanted `move` to be called when the turtle is clicked you would do `t.onclick(move)` instead.


### On key press

If you want something to happen on a key press you can use the `onkey` function. Like `onclick`, `onkey` takes a function that will be called when the key press happens. For this to work, the Turtle screen must have focus. To do this we use `t.listen()` For example:

```
import turtle as t

# Get the screen
screen = t.getscreen()

# Define a function to move the turtle forward
def move_up():
    t.forward(10)

# Call the move_up function when the Up key is pressed
screen.onkey(move_up, "Up")

# Set focus on the screen
t.listen()
```

This will call the function `move_up` function when the up key is pressed.

## The challenge

Copy your script from the previous challenge (call it `PolygonEvents.py` for example) and extend it to use event functions mentioned above:
- When a user clicks on the screen a polygon is draw in that position
- The user could change properties of the next polygon that is drawn has by pressing a key on the keyboard. These properties could include but aren't limited to:
    - The number of sides
    - The colour

## Extension

Create a new script (called `KeyboardTurtle.py`for example) that will allow the user to control the turtle using their keyboard. They could be able to control:
- the turtles movements
- putting the pen up and down
- changing the colour of the pen

## Next

Fancy another? [Challenge - Letters](04-challenge-letters.md)