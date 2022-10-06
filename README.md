# TouchDesigner

this repository will contain various useful TouchDesigner devices and utilities ranging from the simple to the complex.

----------

**Unique Random Sequence Assistant ** (**URSA** for short) offers a variety of ways to generate and navigate non-repeating number sequences. features include:

- dynamically resizable sequences up to 128 steps in length (perfect for MIDI control!)
- increment, decrement and non-destructive reset buttons for navigating sequences
- auto-shuffle feature for generating a new sequence after passing the start of the sequence in either direction and loop lock mode for preventing auto-shuffling
- phase control for scanning through the sequence
- instant update mode for automatically updating the output whenever the seed or phase controls are changed - when off, updates only occur on increment/decrement/reset.
- seed slider with external signal input and new seed button for quickly generating random seeds
- non-unique random mode auto-selects new seed on every step to re-introduce the possibility of repeating numbers
- 3 display modes - current value, histogram and full sequence at a glance
- keyboard shortcuts for quick plug 'n' play action - press 1 to increment, 2 to decrement and 3 to reset
- current value, current count and reset trig outputs for quick and versatile patching

this device and some of its features (esp. loop lock) were inspired by the Mutable Instruments Marbles module created by Émilie Gillet.
