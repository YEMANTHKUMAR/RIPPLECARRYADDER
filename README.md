# RIPPLECARRYADDER
![image](https://github.com/RESMIRNAIR/RIPPLECARRYADDER/assets/154305926/62459000-90cb-4c43-a221-7b8cf1d419b0)
![image](https://github.com/RESMIRNAIR/RIPPLECARRYADDER/assets/154305926/24ea1940-0b55-4f8a-be6a-a7ac5daf2919)
# Full Adder
![image](https://github.com/RESMIRNAIR/RIPPLECARRYADDER/assets/154305926/3208d46f-2fd4-4d6a-987f-63102c173ca0)

VERILOG CODE
````````````````
module ripple carry(S, Co, X, Y, Ci);
  input X, Y, Ci;
  output S, Co;
  wire w1,w2,w3;
  //Structural code for one bit full adder
  xor G1(w1, X, Y);
  xor G2(S, w1, Ci);
  and G3(w2, w1, Ci);
  and G4(w3, X, Y);
  or G5(Co, w2, w3);
endmodule
module ripple carry(S, Cout, X, Y,Cin);
 input [3:0] X, Y;
 input Cin;
 output [3:0] S;
 output Cout;
 wire w1, w2, w3;
 fulladder u1(S[0], w1,X[0], Y[0], Cin);
 fulladder u2(S[1], w2,X[1], Y[1], w1);
 fulladder u3(S[2], w3,X[2], Y[2], w2);
 fulladder u4(S[3], Cout,X[3], Y[3], w3);
endmodule
``````````````````````


OUTPUT


![image](https://github.com/YEMANTHKUMAR/RIPPLECARRYADDER/assets/160569469/2af478a4-ad89-4325-8174-d67678c11434)

