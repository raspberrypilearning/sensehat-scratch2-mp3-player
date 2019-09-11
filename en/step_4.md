## Displaying the track number

Next, you're going to display the number of the track that's currently playing. You can have a go at trying this on your own — use the hints if you get stuck.

--- task ---
Try the following:
1. Create a new variable called `track`{:class="blockdata"}.
   [[[generic-scratch-add-variable]]]
1. Use the `scroll message`{:class="blockmoreblocks"} block to display the number stored in `track`{:class="blockdata"} on the Sense HAT.
1. Play the track with the number stored in your the `track`{:class="blockdata"} variable.
--- /task ---

--- hints --- --- hint ---
You can store a number in `track`{:class="blockdata"} by doing the following:
```blocks
when flag clicked
set [track v] to [1]
play sound [track_01.mp3]
forever
set pixel (pick random (0) to (7)),( pick random (0) to (7)) to R (pick random (0) to (255))G(pick random (0) to (255))B(pick random (0) to (255))::extension
```
--- /hint --- --- hint ---
The `scroll message`{:class="blockmoreblocks"} block can use the `track`{:class="blockdata"} variable with a `join`{:class="blockoperators"} block. You can choose whichever colours you like.
```blocks
when flag clicked
set [track v] to [1]
scroll message (join [track] (track)) at rotation [0 v] in colour [white v] background [off v] ::extension
play sound [track_01.mp3]
forever
set pixel (pick random (0) to (7)),( pick random (0) to (7)) to R (pick random (0) to (255))G(pick random (0) to (255))B(pick random (0) to (255))::extension
```
--- /hint --- --- hint ---
Finish the script by changing the track that is being played to the `track`{:class="blockdata"} variable.
```blocks
when flag clicked
set [track v] to [1]
scroll message (join [track] (track)) at rotation [0 v] in colour [white v] background [off v] ::extension
play sound (track)
forever
set pixel (pick random (0) to (7)),( pick random (0) to (7)) to R (pick random (0) to (255))G(pick random (0) to (255))B(pick random (0) to (255))::extension
```
--- /hint --- --- /hints ---
