## 2016 June 21st, Tuesday

Have added blokok sound for leaping.

## 2016 June 20th, Monday

I've figured out how to turn one sound into an array, so that now the blok hop sounds are perfect.

Now have a jumping ability included, but it needs to be revised for better feel. I want to make it so that just holding space and left or right at the same time makes a big jump - never mind the step-jump previously envisaged.

Now have the blok jumping reasonably well.

## 2016 June 19th, Sunday

First goal: put a block on the screen (just a div with colour). Make it centred vertically and horizontally.

Second goal: make the block jump when you press "w". It should jump and fall according to gravity (m/s^).

For this, it's necessary to have a sense of time. So the code has to count the milliseconds passing each loop.

It seems that Javascript has the ability to update a frame x times per second. That'll do.

I have the blok responding to a keypress now, just moving at a constant speed. What I want is for it to detect when a key is pressed (i.e. when the state *changes* - when space used not to be pressed and is now pressed) and then run a little script.
What the script does is create an initial velocity and then reduce that with an acceleration each frame.

Pseudocode:
~~~~
Keypress_space_then = false
If keypress_space_now != keypress_space_then;
	blokVY = 50;
each _frame:
	blokVelY = blokVelY - 9.81;
	blokPosY = blokPosY + blokVelY;
~~~~

### ACHIEVEMENT UNLOCKED: blokblok 0.0.1:

A blok appears on screen, and when you press a or d, it hops left or right. The blok will not fall below the screen. The blok only jumps if it is planted on the ground, and not repeatedly in the air. Produces sound, though not perfectly - it's currently missing many sound triggers, as though it takes a while to reset itself. Need some ability to overlap sounds.
