---
layout: post
title:  "全加器"
date:   2020-03-15 13:12:36 +0530
categories: Verilog
---
先以一位全加器为例：Xi、Yi代表两个加数，Cin是地位进位信号，Cout是向高位的进位信号。列表有：

Xi|Yi|Cin|Sum|Cout
:--:|:--:|:--:|:--:|:--:
 0 | 0 | 0 | 0 | 0
 0 | 0 | 1 | 1 | 0
 0 | 1 | 0 | 1 | 0  
 0 | 1 | 1 | 0 | 1
 1 | 0 | 0 | 1 | 0
 1 | 0 | 1 | 0 | 1
 1 | 1 | 0 | 0 | 1
 1 | 1 | 1 | 1 | 1


下面是全加器的门级Verilog语言描述：

```verilog
module Fadd(x,y,Cin,Cout,Sum);
  input x,y,Cin;
  output Cout,Sum;
  wire a,b,c;

  xor xor1(a,x,y);
      xor2(Sum,a,Cin);
  and and1(b,x,y);
      and2(c,Cin,a);
  or  or1(Cout,b,c);

endmodule

```

