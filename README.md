# 5-pin-midi
weekend midi project

benvanleeuwen43
5 days ago
sorry if i have gone the wrong way about asking for advice ?
my project is :
a simple MIDI controller, designed to control the parameters of the boss sy-300 guitar synth, it has four buttons, designed to act like the three CTL foot switches on the front of the "SY", The first is osc1 off/on , and two and three toggle up/down between the presets, it includes two potentiometers for parameters such as pitch and detune, the remaining button has proven handy {to date (1 day)} for changing local parameter "waveform" to "detune saw" when it is not already selected in the presets. as the parameter detune is attached to that.
the controller is based on the Amtel mega32U4 chip, and the board is the Duinotech Leonardo Tiny, which leaves only practical wiring access to input pins (D9, D10, D11, A0, A1, A2)
this is not so bad because the SY has only 6 available parameters to control with incoming midi messages ,
though it looks as more options are available, because i saw at one occasion what looked as the SY writing over existing program material which was very confusing !
I also included a 5V voltage regulator (7805) which needed a blocking diode, as usb power was coming from the 5 pin din supply back to the regulator, shown up by my power supply led,
this is essential because the final goal is to run off 9V battery.

so far it has been quite simple to do, once understanding the control surface library, and the requirements of the sy-300,
I am new to Arduino but it is something i always wanted to do.
the ease and simplicity, of the final code was impressive ! and I praise pieter P ? for his fantastic work !

my next goal was to try and initiate a "Pin_Change_Interrupt_Request"
not because the midi controller was not working as expected, because it was actually working very well,

the motive was just to learn a little programming,
the initial motive was because the encoders on the first project, seemed to be running with some latency. at first i thought it was the code?
But after plugging in a musical keyboard into my laptop (HP 2MHZ processor 4gig RAM 64bit operating system Win 8.1)
via USB, and running a software MIDI program VMPK, showed up that the latency was some, still, unresolved computer issue. (which is my next project !)

because I felt the software that comes with the "SY" the Boss Tone Studio, actually was a little bit of a dog, who am i to question ?
and my actual goal was to directly control the parameters of the SY, also the control surface software is so flexible that it is capable of serial type MIDI via 5 pin din !
at the same time as the USB MIDI ! allowing me to run a program called MIDI OX, to de bug, though I could have used the serial de bug included with control surface (but not serial MIDI as well because the serial port is being used), but it was as simple as, to, double forward slash// the irrelevant controller out !
after reserch, it becomes apparent that Arduino is not able to interrupt an analogue input.
I now have a Pro Mirco,
how would you go about pin change interrupts for two encoders wired to pins (8,9 + 10,15) ?

thank you for any time invested into my cause

Ben !

