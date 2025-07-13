module RAM(wr,din,dout,clk,addr);
  input clk,wr;
  input [7:0]din;
  input [2:0]addr;
  output reg [7:0]dout;
  
  reg [7:0]memory[7:0];
  
  always @(posedge clk)begin
    if(wr)begin
      memory[addr]<=din;
    end
    else begin
      dout<=memory[addr];
    end
  end
endmodule
