### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

• Write and draw th e Digital lo gic system.  
• Write t he Verilog code for above system .  
• Enter th e Verilog c ode in Xilinx softwar e.  
• Check the syntax a nd simulat e the above verilog cod e (using ModelSim or Xilinx) 
and verify the outp ut waveform as obtain ed.  
• Implem ent the above code in Spartan II u sing FPGA kit.

**PROGRAM**
```
/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:Kavidharshini
RegisterNumber:25012397
```
```
module exp11(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out+1;
end
endmodule
```

**RTL LOGIC UP COUNTER**

<img width="462" height="265" alt="image" src="https://github.com/user-attachments/assets/36a1be3f-630e-474a-bc08-d69df3416ea3" />


**TIMING DIAGRAM FOR IP COUNTER**

<img width="1008" height="290" alt="image" src="https://github.com/user-attachments/assets/87049dfb-001b-4e57-a8f7-d1c6f1fa9e68" />


**TRUTH TABLE**

<img width="1005" height="522" alt="image" src="https://github.com/user-attachments/assets/6d12e7d4-1df8-43b2-b749-e0678d910924" />


**RESULTS**

Hence implemented 4 bit synchronous up counter and validate functionality.
