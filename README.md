# -adder-circuit

*2 bit adder*

A1  A0
  + B1  B0
____
  C  X1 X0
____
-------------------


__A           B             X        C

A1 A0  B1 B0    X1 X0     C

0   0     0    0      0    0      0
0   0     0    1      0    1      0
0   0     1    0      1    0      0
0   0     1    1      1    1      0
0   1     0    0      0    1      0
0   1     0    1      1    0      0
0   1     1    0      1    1      0
0   1     1    1      0    0      1
1   0     0    0      1    0      0
1   0     0    1      1    1      0
1   0     1    0      0    0      1
1   0     1    1      0    1      1
1   1     0    0      1    1      0
1   1     0    1      0    0      1
1   1     1    0      0    1      1
1   1     1    1      1    0      1

X0 =  A1'.A0'.B1'.B0    +   A1'.A0'.B1.B0   +   A1'.A0.B1'.B0'   +   A1'.A0.B1.B0'   +    A1.A0'.B1'.B0    +    A1.A0'.B1.B0   +    A1.A0.B1'.B0'   +    A1.A0.B1.B0'  =     A1'.A0'.B0     +      A1'.A0.B0'     +     A1.A0'.B0    +    A1.A0 .B0'

*X0  =  A0.B0'    +     A0'.B0   =  (A0     xor   B0)*

X1 =  A1'.A0'.B1.B0'    +  A1'.A0'.B1.B0   +    A1'.A0.B1'.B0   +   A1'.A0.B1.B0'     +    A1.A0'.B1'.B0'   +    A1.A0'.B1'.B0     +     A1.A0.B1'.B0'   +     A1.A0.B1.B0  =  A1'.A0'.B1    +   A1.A0'.B1'   +     A1.A0.(B1  xnor   B0)    +   A1'.A0.(B1  xor  B0)


X1 = A0'.(A1   xor  B1)    +     A1.A0.(B1   xnor   B0)    +    A1'.A0.(B1   xor   B0)

*X1 = A0.(A1  xor  B1  xor  B0)   +    A0'.(A1 xor B1)*


C = A1.A0.B1   +   A1.A0'.B1    +   A0.B0.(A1  xor  B1)

*C =  A1.B1   +   (A0.B0.(A1  xor  B1))*


*Arjun ( Isuru ) 🍁✨*
