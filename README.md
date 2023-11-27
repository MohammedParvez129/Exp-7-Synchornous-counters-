# Exp-6-Synchornous-counters - up counter and down counter 
### AIM: To implement 4 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## UP COUNTER 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)

## DOWN COUNTER 

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.
![image](https://user-images.githubusercontent.com/36288975/169644844-1a14e123-7228-4ed8-81a9-eb937dff4ac8.png)


4-bit Count Down Counter
### Procedure

1.Create a new project in QuartusII software.
2.Name the project as uc for upcounter and dc for down counter.
3.Create a new verilog hdl file in the project file.
4.Name the module as dc and uc for down counter and up counter.
5.Within the module declare input and output variables.
6.Create a loop using if-else with condition parameter as reset value.
7.End the loop.
8.End the module.

### PROGRAM 

Program for flipflops  and verify its truth table in quartus using Verilog programming.

Developed by : MOHAMMED PARVEZ S

Register Number : 23010483

Code :

UP COUNTER :

![Exp6 upc code](https://github.com/MohammedParvez129/Exp-7-Synchornous-counters-/assets/143175737/67b2684c-7333-4011-951b-4d1becb6b826)

DOWN COUNTER :

![Exp6 doc code](https://github.com/MohammedParvez129/Exp-7-Synchornous-counters-/assets/143175737/92c8c998-82b2-42c9-b667-98b2cca9079a)

RTL realization : 

UP COUNTER :

![Exp5 upc RTL diagram](https://github.com/MohammedParvez129/Exp-7-Synchornous-counters-/assets/143175737/41e6698c-c2b5-4f03-98a4-48cfd5af8d1e)

DOWN COUNTER :

![Exp5 doc RTL diagram](https://github.com/MohammedParvez129/Exp-7-Synchornous-counters-/assets/143175737/cbd835b8-b24d-4947-a6c9-be88aa07806d)

Truth Table : 

UP COUNTER :

![277085989-3bb80ba1-802f-4b29-9b05-e2883755bb61](https://github.com/MohammedParvez129/Exp-7-Synchornous-counters-/assets/143175737/491447f0-79b8-4ac8-a507-0e6388af16b8)

DOWN COUNTER :

![277085999-26e364d2-d30e-48f8-9e46-5ceeb264fe4d](https://github.com/MohammedParvez129/Exp-7-Synchornous-counters-/assets/143175737/9f4706dc-1202-4898-8c19-dcafa332433c)

## OUTPUT 

UP COUNTER :

![279425738-32c085a6-28b6-471b-a0f6-f4eaf69998ee](https://github.com/MohammedParvez129/Exp-7-Synchornous-counters-/assets/143175737/1f7ab0b8-0526-4479-919e-f055e4c69d8e)

DOWN COUNTER :

![279425473-715ea572-9659-4786-a87d-e490376a0ffd](https://github.com/MohammedParvez129/Exp-7-Synchornous-counters-/assets/143175737/502531e9-b6c4-467a-8308-a84cf758132c)

### RESULTS 
Thus Synchornous counters up counter and down counter circuit are studied and the truth table for different logic gates are verified.
