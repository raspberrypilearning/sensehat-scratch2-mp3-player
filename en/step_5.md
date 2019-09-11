## Changing the volume

You can now add some extra controls to your MP3 player. First of all, set up your script so that the Sense HAT joystick can control the volume.

The Raspberry Pi treats the Sense HAT joystick in the same way as the arrow keys on your keyboard. This means that, for example, pushing the joystick up is the same as pushing the up arrow on your keyboard.

--- task ---
Change the script you already have so that the volume starts at `100%`.
```blocks
when flag clicked
set [track v] to [1]
scroll message (join [track] (track)) at rotation [0 v] in colour [white v] background [off v] ::extension
set volume to (100) %
play sound (track)
forever
set pixel (pick random (0) to (7)),( pick random (0) to (7)) to R (pick random (0) to (255))G(pick random (0) to (255))B(pick random (0) to (255))::extension
```
--- /task ---

--- task ---
Add in two new scripts that use `when key pressed`{:class="blockcontrol"} blocks to `change volume`{:class="blocksound"}.

```blocks
when [up arrow v] key pressed
change volume by (10)

when [down arrow v] key pressed
change volume by (-10)
```
--- /task ---

Test your scripts again: click the green flag, and then use the Sense HAT joystick to change the volume of your music.
