# Vlsi-6
module gates_ff(

    input in1,

    input in2,

    output out1,

    output out2,

    output reg q,

    input clk,

	 input rst

    );



assign out1=in1^in2;

assign out2=out1&in2;



always @(posedge clk) begin

if (rst) 

	q=0;

else if (clk==1)

	q=in1;

end



endmodule

