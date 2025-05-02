# Quiz System Using Analog and Digital ICs
This is an interactive project implemented using both software simulation and hardware prototyping. 
The system is divided into three main functional blocks:

## Random Number Generator
-Uses IC 4017 (Decade Counter) to generate numbers from 1 to 6.
-The output is passed through a diode-based combinational logic to perform BCD to Binary conversion.
-The Binary output is then decoded using IC 7447 (Binary to Seven Segment Decoder).
-The decoded outputs drive a Seven Segment Display to show the random number.
-A 555 Timer IC is used to generate the clock for the IC 4017.
-Timer configuration: ~45 MHz using a 10µF capacitor and 150kΩ resistors.

## Fastest Finger First Module
-Consists of four identical circuits, each representing a player.
-All circuits are connected to a common Set and Reset rail.
-When any player presses their button:
-Their 555 Timer output goes HIGH.
-All other inputs are locked out to prevent false triggering.
-A common Reset button is used to reset all 555 timers to LOW for the next round.

## Scoreboard
-Uses IC 4026 (BCD to Seven Segment Decoder with Counter).
-Each pulse input increments the score.
-The current score is displayed on a Seven Segment Display.
-Can be expanded to multiple digits if needed.

## Power Supply
A regulated 5V supply is required.
A 9V battery can be used with a voltage regulator circuit to step down to 5V for consistent performance.



AAll corresponding circuit diagrams, simulation results, and hardware implementation photos are provided in the repository.
