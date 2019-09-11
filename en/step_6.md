## Changing the track

Now that you know how to use the joystick, it's time to try and use it to change which track is playing.

--- task ---
1. When the program starts, you will need to `stop all sounds`{:class="blocksound"}.
2. Use the `when left arrow is pressed`{:class="blockevents"} and the `when right arrow is pressed`{:class="blockevents"} blocks to `stop all sounds`{:class="blocksound"} and to increase or decrease the value of your `track`{:class="blockdata"} variable.
3. You can also use a `scroll message`{:class="blockmoreblocks"} block to show again which track is being played.
--- /task ---

--- hints --- --- hint ---
Adding a single block will complete your main script:
```blocks
when flag clicked
set [track v] to [1]
scroll message (join [track] (track)) at rotation [0 v] in colour [white v] background [off v] ::extension
stop all sounds
set volume to (100) %
play sound (track)
forever
set pixel (pick random (0) to (7)),( pick random (0) to (7)) to R (pick random (0) to (255))G(pick random (0) to (255))B(pick random (0) to (255))::extension
```
--- /hint --- --- hint ---
You can use the `when arrow is pressed`{:class="blockevents"} blocks to change the value stored in your `track`{:class="blockdata"} variable like this:
```blocks
when [right arrow v] key pressed
stop all sounds
change [track v] by (1)

when [left arrow v] key pressed
stop all sounds
change [track v] by (-1)
```
--- /hint --- --- hint ---
Then you just need to `scroll message`{:class="blockmoreblocks"} and `play sound`{:class="blocksound"} for both arrow keys.

```blocks
when [right arrow v] key pressed
stop all sounds
change [track v] by (1)
scroll message (join [track] (track)) at rotation [0 v] in colour [white v] background [off v] ::extension
play sound (track)

when [left arrow v] key pressed
stop all sounds
change [track v] by (-1)
scroll message (join [track] (track)) at rotation [0 v] in colour [white v] background [off v] ::extension
play sound (track)
```
```
--- /hint --- --- /hints ---

That's it — your MP3 player is complete! Click on the green flag and then have a go at changing your tracks using the Sense HAT joystick.
