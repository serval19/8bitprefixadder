module prefix_adder_8bit (
  input [7:0] A,
  input [7:0] B,
  output [8:0] Sum
);

  assign Sum[8] = A[7] & B[7];
  assign Sum[7] = A[7] ^ B[7];
  assign Sum[6] = A[6] ^ B[6];
  assign Sum[5] = (A[6] & B[6]) | (A[5] & B[5]);
  assign Sum[4] = A[4] ^ B[4];
  assign Sum[3] = (A[4] & B[4]) | (A[3] & B[3]);
  assign Sum[2] = A[2] ^ B[2];
  assign Sum[1] = (A[2] & B[2]) | (A[1] & B[1]);
  assign Sum[0] = A[0] ^ B[0];

endmodule
