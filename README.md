# SR-FLIPFLOP-USING-CASE

**AIM:**

To implement  SR flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/0f710028-ad52-4d3e-9276-8714cf023a25)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dabfc4f4-87e3-4cbc-9472-f89ee1b5ed30)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dd90d16c-aec5-4290-a586-e2346b1e9eb5)

 
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/473efad6-d70b-4ca7-aeb7-898bbfca319f)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.

    module sr_ff (s, r, clk, rst, q);
      input s, r, clk, rst;
      output reg q;

      always @(posedge clk or posedge rst)
    begin
        if (rst)
         q <= 0; // Reset the flip-flop
        else
    begin
          case ({s, r}) // S and R control the behavior
            2'b00: q <= q;    // No change
            2'b01: q <= 0;    // Reset
            2'b10: q <= 1;    // Set
            2'b11: q <= 0;    // Invalid state, typically treated as reset
          endcase
        end
      end
    endmodule



Developed by: VISHNU RATHAN.B

RegisterNumber:24001855

**RTL LOGIC FOR FLIPFLOPS**

![exp6 rtl](https://github.com/user-attachments/assets/9ec08065-3a35-4bb8-b1da-2337a77e324a)


**TIMING DIGRAMS FOR FLIP FLOPS**

![exp6op](https://github.com/user-attachments/assets/62384dc4-2aed-43fe-9e97-f656b9dca7d6)


**RESULTS**

Thus the SR flipflop is implemented using verilog and validated their functionality using their functional tables
