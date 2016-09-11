# HW2: Stress Release Bubble Wrap KeyBoard
In this HW, a stress release keyboard is constructed using ReadBear Duo board, bubble wrap, and cupper wires. The text entry technique is first tested using switches mounted in a breadboard, once it was working well, a keyboard constructed in a relax bubble wrap material was implemented and tested. Enjoy and relax.

## What text entry technique you chose and why?
The technique used here is similar to a five-key technique in the sence that five keys are used, but it is also similar to multi-tap technique because, in order to choose a letter, the user need to press more than once the switches. However, the technique implemented does not need too many pressing of switches as in a five-key technique (like from going from A to K, 9 pressing) or multi-tap (7 pressing to choose S, if only five switches are used). It uses less pressing, because as you choose a certain group, that group sub-devided itself into four new group; then, no more than three pressing are needed to choose a letter. The following figures shows an example while choosen the letter R:

There are four switches for each group:
1. Switch 1: ABCDEF
2. Switch 2: GHIJKL
3. Switch 3: MNOPQRS
4. Switch 4: TUVWXYZ

Fifth siwtch is for space.
![KeyBoard Initial State](https://drive.google.com/drive/u/0/folders/0Bwp10bnNHRKxTkhoR1FMZUFmUTg)

Once one choose group 3, using switch 3, the keyboard screen looks like this:


Then again swith 3 is pressed, and keyboard screen looks like:

-------
| |Q|
-------
| | |R|
-------
| ||
-------

Finally switch 2 is pressed, and letter R is choosen. Then, no more than 3 pressing are need. Therefore this technique is like a binary encoding since 3 bits are needed, and can be used for 2^8 options.


