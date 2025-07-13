module tb_RAM;
  reg clk;
  reg wr;
  reg [7:0] din;
  reg [2:0] addr;
  wire [7:0] dout;

  RAM uut (
    .wr(wr),
    .din(din),
    .dout(dout),
    .clk(clk),
    .addr(addr)
  );

  initial begin
    clk = 0;
    forever #5 clk = ~clk;
  end

  initial begin

    wr = 1;
    din = 8'd0;
    for (int i = 0; i < 8; i++) begin
      addr = i[2:0];
      din = i * 8;
      $display("Addr=%0d | Data=%0d", addr, din);
      #10;
    end

    wr = 0;
    for (int i = 0; i < 8; i++) begin
      addr = i[2:0];
      #10;
      $display("Addr=%0d | Data=%0d", addr, dout);
    end

    $finish;
  end
endmodule
