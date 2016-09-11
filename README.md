# HW2: Stress Release Bubble Wrap KeyBoard
In this HW, a stress release keyboard is constructed using ReadBear Duo board, bubble wrap, and cupper wires. The text entry technique is first tested using switches mounted in a breadboard, once it was working well, a keyboard constructed in a relax bubble wrap material was implemented and tested. Enjoy and relax.

## What text entry technique you chose and why?

The technique used here is similar to a five-key technique in the sence that five keys are used, but it is also similar to multi-tap technique because, in order to choose a letter, the user need to press more than once the switches. However, the technique implemented does not need too many pressing of switches as in a five-key technique (like from going from A to K, 9 pressing) or multi-tap (7 pressing to choose S, if only five switches are used). It uses less pressing, because as you choose a certain group, that group sub-devided itself into four new group; then, no more than three pressing are needed to choose a letter. The following figures shows an example while choosen the letter R:

There are four switches for each group:

1. Switch 1: ABCDEF

2. Switch 2: GHIJKL

3. Switch 3: MNOPQRS

4. Switch 4: TUVWXYZ

Fifth switch is for space:

![](https://googledrive.com/host/0Bwp10bnNHRKxTkhoR1FMZUFmUTg/keyboard1.png)

Once one choose group 3, using switch 3, the keyboard screen looks like this:

![](https://googledrive.com/host/0Bwp10bnNHRKxTkhoR1FMZUFmUTg/keyboard2.png)

Then again switch 3 is pressed, and keyboard screen looks like:

![](https://googledrive.com/host/0Bwp10bnNHRKxTkhoR1FMZUFmUTg/keyboard3.png)

Finally switch 2 is pressed, and letter R is choosen. Then, no more than 3 pressing are need. Therefore this technique is like a binary encoding since 3 bits are needed, and can be used for 2^8 options.

# How you implemented character recognition?

First, five switches are used, and implemented using interrups and deboucing, in the same manner as the example in [button_interrupt_debounce.ino](https://github.com/bjo3rn/idd-examples/tree/master/redbearduo/examples/button_interrupt_debounce).

The volatile variables **updatekeyboard** and **buttonpressed** are used to keep track and recognize the character. Once a switch is pressed, **updatekeyboard** value change to 1 and **buttonpressed** gets the value of the switch pressed. This happen in the function 'void toggle()'. In the function 'void loop()', **updatekeyboard** is checked, if it is 1, then switch information is updated. First the code check if switch 5 is pressed, if it is pressed, space is the character choosen. If not, then we have three different states: **state0**,**state1** and **state2**. If state does not have value (that is 0) then it get the value of **buttonpressed**, the priority is first for **state0**, then **state1** and finally **state2** Once all states have a value, the character is choosen and added to the final total string. 'switch' functions are use for the decoding of the state values. Finally, "HELLO WORLD" can be obtained.

![](https://googledrive.com/host/0Bwp10bnNHRKxTkhoR1FMZUFmUTg/helloworldhw2.png)

# How you constructed the physical device?

First, an array of switches were constructed in a breadboard, so the code could be implemented and tested. The switches are implemented is a 10kOhm resistance in series for protection, the picture is self-explanatory:

![](https://googledrive.com/host/0Bwp10bnNHRKxTkhoR1FMZUFmUTg/IMG_4179.jpg)

The test video for the first design can be found in:

[VIDEO TEST BREADBOARD](https://drive.google.com/drive/u/0/folders/0Bwp10bnNHRKxZUp4dEtjd1dUeG8).

Once the breadboard was constructed, the stress release bubble wrap keyboard was constructed. It was build using three layer of bubble wrap, the back layer has the lines for VDD, and the front layer has 5 lines which are used for the switches. The lines were consctructed using cupper tape. Then, small holes (approximatly 2x2mm) were made in the middle bubble wrap layer. 

![](https://googledrive.com/host/0Bwp10bnNHRKxTkhoR1FMZUFmUTg/IMG_4182.jpg)
![](https://googledrive.com/host/0Bwp10bnNHRKxTkhoR1FMZUFmUTg/IMG_4181.jpg)

One a user is relaxing with the wrap, and press it enough, the electrodes in the first and third layer connect through the hole in the middle layer, acting as switches:

![](https://googledrive.com/host/0Bwp10bnNHRKxTkhoR1FMZUFmUTg/IMG_4183.jpg)
![](https://googledrive.com/host/0Bwp10bnNHRKxTkhoR1FMZUFmUTg/IMG_4185.jpg)

Finally, the video test for the stress release bubble wrap keyboard is found in the following link:

[VIDEO TEST "stress release bubble wrap keyboard"](https://drive.google.com/drive/u/0/folders/0Bwp10bnNHRKxZUp4dEtjd1dUeG8).
