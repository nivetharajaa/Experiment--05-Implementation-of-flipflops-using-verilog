# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: 
To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  
PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   
Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */

STEP 1: Open Quartus II and select new project and choose the file location.

STEP 2: Module Declaration. Module should have the file name.

STEPS 3: Input-Output Delecaration.

STEPS 4: Use assign declaration and wire to define the functionality of logic circuits.

STEP 5: At the end give endmodule.

STEP 6: Run the program and choose RTL viewer to get RTL realization


### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by:A.NIVETHA 
RegisterNumber:212222230101  
*/
## SR FLIPFLOPS CODE:

module ex5(S,R,clk,Q,Qbar);

input S,R,clk;

output reg Q;

output reg Qbar;

initial Q=0;

initial Qbar=1;

always @(posedge clk)

begin

Q=S|((~R)&Q);

Qbar=R|((~S)&(Qbar));

end

endmodule

## SR FLIPFLOPS CODE:

module ex5(S,R,clk,Q,Qbar);

input S,R,clk;

output reg Q;

output reg Qbar;

initial Q=0;

initial Qbar=1;

always @(posedge clk)

begin

Q=S|((~R)&Q);

Qbar=R|((~S)&(Qbar));

end

endmodule
## D FLIPFLOPS CODE:

module ex5(D,clk,Q,Qbar);

input D,clk;

output reg Q;

output reg Qbar;

initial Q=0;

initial Qbar=1;

always @(posedge clk)

begin

Q=D;

Qbar=~D;

end

endmodule
## T FLIPFLOPS CODE:

module ex5(T,clk,Q,Qbar);

input T,clk;

output reg Q;

output reg Qbar;

initial Q=0;

initial Qbar=1;

always @(posedge clk)

begin

Q=(T&(~Q))|((~T)&Q);

Qbar=((~T)&Qbar)|(T&(~Qbar));

end

endmodule


### RTL LOGIC FOR FLIPFLOPS 
### RTL FOR SR

![277667626-6afdba53-0b8f-4919-aa6e-b6ba487106bf](https://github.com/nivetharajaa/Experiment--05-Implementation-of-flipflops-using-verilog/assets/120543388/24850588-684d-4662-9076-c44881999bff)

### RTL FOR JK

![277667817-416519ad-8454-45e8-b318-53ae395adf04](https://github.com/nivetharajaa/Experiment--05-Implementation-of-flipflops-using-verilog/assets/120543388/4755ec39-1e99-476e-9eff-0d5f6324def8)

### RTL FOR D:

![277667962-fa2b0cff-1a57-4799-88ae-8fa92c512a3e](https://github.com/nivetharajaa/Experiment--05-Implementation-of-flipflops-using-verilog/assets/120543388/896e55d9-14c8-4435-a327-d86c574de403)

### RTL FOR T:

![277668079-5570644a-0275-4999-a085-121dcbd3d75d](https://github.com/nivetharajaa/Experiment--05-Implementation-of-flipflops-using-verilog/assets/120543388/b6f3f8d3-11b1-4b78-ae0c-02cff821f1dc)


### TIMING DIGRAMS FOR FLIP FLOPS 

### WAVEFPRM FOR SR:
![277668627-b071487d-dd61-467b-9a1f-cddb878628b3](https://github.com/nivetharajaa/Experiment--05-Implementation-of-flipflops-using-verilog/assets/120543388/54b5c5fd-42ce-4711-890c-ebc76736f367)

### WAVEFPRM FOR JK:
![277668731-42a34962-8a37-4fcc-83fd-79c252e740a8](https://github.com/nivetharajaa/Experiment--05-Implementation-of-flipflops-using-verilog/assets/120543388/42688274-dacc-4414-8d17-611c1863c20f)

### WAVEFPRM FOR JK_TOGGLE:
![277669175-e007d92f-bed9-49d2-bc22-38d4416ed433](https://github.com/nivetharajaa/Experiment--05-Implementation-of-flipflops-using-verilog/assets/120543388/f3a3d9bd-c11e-491f-a971-4f656060c052)

### WAVEFPRM FOR D:

![277669251-537b703b-c726-4e9b-b9ac-d22745f8e109](https://github.com/nivetharajaa/Experiment--05-Implementation-of-flipflops-using-verilog/assets/120543388/ade5bfa7-4d62-4a59-99a6-c47ac4cd4c42)

### WAVEFPRM FOR T:

![277669251-537b703b-c726-4e9b-b9ac-d22745f8e109](https://github.com/nivetharajaa/Experiment--05-Implementation-of-flipflops-using-verilog/assets/120543388/a6588108-c6f8-418d-a265-a938d86123dc)

### RESULTS 

Implementation-of-flipflops-using-verilog successfully completed.
