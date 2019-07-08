# Data-types

# Enumeration

  Enumeration is a useful way of defining abstract variables.
  Define an enumeration with "enum"
  
        enum{red,green,yellow} trafic_light1, trafic_light2;
       
  Values can be cast to integer types and auto incremented
  
        enum{a=5,b,c} vars;  //b=6, c=7
        
  A sized constant can be used to set size of the type.
  
        enum bit [3:0] {bronze=4'h3, silver,gold} medal; //all medal members are 4-bits
