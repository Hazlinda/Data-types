# Data-types

# Enumeration

  Enumeration is a useful way of defining abstract variables.
  Define an enumeration with "enum"
  
        enum{red,green,yellow} trafic_light1, trafic_light2;
       
  Values can be cast to integer types and auto incremented
  
        enum{a=5,b,c} vars;  //b=6, c=7
        
  A sized constant can be used to set size of the type.
  
        enum bit [3:0] {bronze=4'h3, silver,gold} medal; //all medal members are 4-bits


# User Define Data Type

In complex testbench some variable declaration might have a longger data-type specification or require to be used in multiple places in the testbench.

In such cases we can use a typedef to give a user-defined name to an existing data type. The new data-type can be used throughout the code and hence avoids the need to edit in multiple places if required. 


    module tb;
    // Declare an alias for this long definition
      typedef shortint unsigned u_shorti;
      typedef enum {RED, YELLOW, GREEN} e_light;
      typedef bit [7:0] ubyte;
  
      initial begin
        u_shorti data = 32'hface_cafe;
        e_light	light = GREEN;
        ubyte cnt = 8'hFF;
    
        $display ("light=%s data=0x%0h cnt=%0d", light.name(), data, cnt);
      end
    endmodule
    
    
