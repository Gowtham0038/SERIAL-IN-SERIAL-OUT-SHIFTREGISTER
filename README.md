# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**
Type the program in Quartus software.

1.Compile and run the program.

2.Generate the RTL schematic and save the logic diagram.

3.Create nodes for inputs and outputs to generate the timing diagram.

4.For different input combinations generate the timing diagram.

/* write all the steps invloved */

**PROGRAM**
~~~
module Exp10(clk, sin, q);

input clk;

input sin;

output [3:0] q;

reg [3:0] q;

always @(posedge clk)

begin

q[0] <= sin;

q[1] <= q[0];

q[2] <= q[1];

q[3] <= q[2];

end endmodule
~~~
/* Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by:Gowtham C
RegisterNumber: 24002349

*/

**RTL LOGIC FOR SISO Shift Register**
![398191488-cb3999ad-3908-4f4d-9451-776c444ee02b](https://github.com/user-attachments/assets/86bdbc6c-9d2c-41f7-bcae-0634a03929f8)

**TIMING DIGRAMS FOR SISO Shift Register**
![398191595-0c1af6f9-2e10-494f-a998-8c7102af78b0](https://github.com/user-attachments/assets/44e9d043-de4b-44f8-99b6-891a8f7108af)

**RESULTS**
Thus to implement SISO Shift Register using verilog and validating their functionality using their functional tables done successfully.
