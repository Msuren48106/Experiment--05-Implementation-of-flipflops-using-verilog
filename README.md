# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![Screenshot 2023-11-26 165020](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/7828acf0-0ce4-4e77-8d85-7d5e395808a2)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![Screenshot 2023-11-26 164713](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/aa118244-6599-49d6-b1ea-994a61334b75)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State

![Screenshot 2023-11-26 164934](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/50ab9926-146f-4d09-92c3-0b623fb06fb9)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
![download](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/583254c5-ba30-4cb8-8ed5-d6be3b67aa32)


 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![Screenshot 2023-11-26 204625](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/9dda7f69-6860-4e12-9025-2bb71bc3def3)


![Screenshot 2023-11-26 204555](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/6a685749-db25-477c-97ed-6c1cb5322fbe)


Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D


![Screenshot 2023-11-26 204800](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/901c2b01-2e83-4845-a1cf-80ea143f20e8)


Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

 ![Screenshot 2023-11-26 210428](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/3ce995ec-6c0d-41d6-9cc6-2fb03802d082)

This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![Screenshot 2023-11-26 210447](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/488c7aef-c1c6-4624-b981-9ac6c880aea0)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 ![Screenshot 2023-11-26 210612](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/36f55f3f-c083-44c2-adee-bf1a116b9efe)


The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.


![Screenshot 2023-11-26 170739](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/7011ce3a-d3ae-4029-a101-cb36472083f5)


This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State

![Screenshot 2023-11-26 170613](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/cd20bbec-7dfb-4f87-8da8-ddb2c6a0696f)


From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: 
RegisterNumber:  
*/






### RTL LOGIC FOR FLIPFLOPS 









### TIMING DIGRAMS FOR FLIP FLOPS 







![Screenshot 2023-11-26 170721](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/b692e43d-97f1-48ff-b98b-5b5a821d8696)

### Truth table
![download](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/6247b71c-3f59-4924-998f-91497f2cd4c6)

![download](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/b52b472e-fdbd-4b6a-90a2-85652635f73e)

![download](https://github.com/vamsikrishna272005/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147477015/cb41b168-057f-4f9e-a446-803295ff71a1)


### RESULTS 
