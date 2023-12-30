`timescale 1ns/1ns

module testbench_prefix_adder_8bit;

  reg [7:0] A;
  reg [7:0] B;
  wire [8:0] Sum;

  // Instantiate the 8-bit parallel prefix adder
  prefix_adder_8bit uut (
    .A(A),
    .B(B),
    .Sum(Sum)
  );

  // Clock generation
  reg clk;
  always #5 clk = ~clk;

  // Testbench stimulus
  initial begin
    // Initialize inputs
    A = 8'b11011010;
    B = 8'b10100111;

    // Apply inputs and observe outputs for 16 clock cycles
    repeat (16) begin
      #1 A = $random;
      #1 B = $random;
      #1;
      $display("Time %t: A = %b, B = %b, Sum = %b", $time, A, B, Sum);
    end

    // End simulation
    $finish;
  end
initial begin 
  $dumpfile("dump.vcd");
  $dumpvars(1);
end
endmodule
