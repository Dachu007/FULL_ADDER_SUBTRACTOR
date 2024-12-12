# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

Full Adder


![9d04ddcc-26b3-4a15-9253-b16416b64e3a](https://github.com/user-attachments/assets/3e8b1f08-7600-4f3d-b5fc-f01aba81c2fb)

Full Subtractor


![b122fc2a-4009-42bd-b978-de761e9c4ea3](https://github.com/user-attachments/assets/2eaa4195-6371-4887-8d0f-ba00bcc1e997)

**Procedure**

write the detailed procedure here

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Full Adder

```
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```

Full Subtractor

```
module fs(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff= ( (a ^ b)^bin);
assign borr= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```




Developed by: Dharshini S RegisterNumber:24900257


**RTL Schematic**

Full Adder

![Screenshot (19)](https://github.com/user-attachments/assets/fae7da49-5dfd-4030-84e0-e296386b4088)

Full Subtractor

![Screenshot (21)](https://github.com/user-attachments/assets/612fb173-3650-4f45-98b5-1e911c9d9365)



**Output Timing Waveform**

Full Adder
![Screenshot (20)](https://github.com/user-attachments/assets/f1f4a96d-c3b6-4e79-a8ac-9bc6f8780142)

Full Subractor
![Screenshot (22)](https://github.com/user-attachments/assets/7671dcb9-6913-4581-84f7-137c865c886e)





**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



