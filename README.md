"# -hw2-2" 
"# -hw2-2" 
# -hw2-2
module Decoder_3*8(
    input x,y,z;
    output [7:0] D;
)
    wire [2:0] D0_wire,D1_wire,D2_wire,D3_wire,D4_wire,D5_wire,D6_wire,D7_wire,z_not,y_not,x_not;
    and G0(D0_wire,x_not,y_not,z_not);
    and G1(D1_wire,x_not,y_not,z);
    and G2(D2_wire,x_not,y,z_not);
    and G3(D3_wire,x_not,y,z);
    and G4(D4_wire,x,y_not,z_not);
    and G5(D5_wire,x,y_not,z);
    and G6(D6_wire,x,y,z_not);
    and G7(D7_wire,x,y,z);
    not G8(z_not,z);
    not G9(y_not,y);
    not G10(x_not,x);
endmodule


