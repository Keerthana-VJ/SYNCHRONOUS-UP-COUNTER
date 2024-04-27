# SYNCHRONOUS-UP-COUNTER
## DEVELOPED BY: KEERTHANA.V
## REGISTER NUMBER: 212223220045

## AIM:

To implement 4 bit synchronous up counter and validate functionality.

## SOFTWARE REQUIRED:

Quartus prime

## THEORY:

## 4 bit synchronous UP Counter:

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

## Procedure:

```
1.Initialize the shift register to a known state (e.g., all zeros).

2.Input a bit serially into the shift register.

3.Shift the contents of the register one position to the right (or left).

4.Output the shifted bit from the last stage of the register.

5.Repeat steps 2-4 for each bit you want to input and shift.
```

## PROGRAM:
 Program for flipflops and verify its truth table in quartus using Verilog programming. 

```
module exp11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(!rstn)
     out<=0;
   else 
     out <= out+1;
end
endmodule
```
## RTL LOGIC UP COUNTER:
![325559752-6766a5b3-e8be-425b-8991-9c1564ec02fb](https://github.com/Keerthana-VJ/SYNCHRONOUS-UP-COUNTER/assets/149347704/04e3c990-074d-4ae5-99d7-5c2b79b4bc3e)

## TIMING DIAGRAM FOR IP COUNTER:

![325559934-ab6c6174-1052-4905-a271-09797eae8c39](https://github.com/Keerthana-VJ/SYNCHRONOUS-UP-COUNTER/assets/149347704/128de7b7-6e57-42d8-a27e-34600aa0275c)

## TRUTH TABLE:
![325559984-e3f2a515-5eb9-4e89-b1a3-e7f134578777](https://github.com/Keerthana-VJ/SYNCHRONOUS-UP-COUNTER/assets/149347704/b75ef146-b4c8-4718-87fa-c3d60f2c4dce)


## RESULTS:
Thus the program executed successfully.
