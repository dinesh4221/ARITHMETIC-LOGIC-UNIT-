======TO PERFORM ADDITION=======

We give the input's to the parallel adder circuit.
we will connect the CIN(LSB)  to ground and the carry obtained is connected to the succeeding CIN.

S6/CONTROL-GROUND
S11-CONNECTED TO CONTROL/S6
S10-CONNECTED TO VCC/V
S13,S14,S15-CONNECTED TO NEXT CIN

--OUTPUT LCD'S-
 
U9-LSB,U10,U11,U12,U17-CARRY

=====TO PERFORM SUBTRACTION=====

We give the input's to the parallel adder circuit.
We take the 2's complement of the subtrahend by giving CIN-(LSB) as 1 and inverting the 
subtrahend with a XOR gate.
Then the carry obtained is connected to the succeeding CIN.
If the final carry obtained is 1,then we ignore the carry and the value obtained is positive else we take the 2's complement of the obtained value and it is negative.

S6/CONTROL-VCC/V
S11-CONNECTED TO CONTROL/S6
S10-CONNECTED TO VCC/V
S13,S14,S15-CONNECTED TO NEXT CIN

--OUTPUT LCD'S
U9-LSB,U10,U11,U12,U17-sign

=====XOR=====

We give the input's to the parallel adder circuit.
For performing the logical operation XOR we make the CIN's 0 and the sum obtained at each full adder is the output (since the sum obtained is the XOR of the INPUTS)

S6/CONTROL-GROUND
S11-CONNECTED TO CONTROL/S6
S10-GROUND
S13,S14,S15-CONNECTED TO NEXT CIN

---OUTPUT LCD'S-

U9,U10,U11,U12

=====AND=====

We give the input's to the parallel adder circuit.
For performing the logical operation AND we make the CIN's 0 and the carry obtained at each full adder is the output (since carry=AB + B Cin + A Cin and Cin is 0 so carry=AB.) 

S6/CONTROL-GROUND
S11-CONNECTED TO CONTROL/S6
S10-GROUND
S13,S14,S15-CONNECTED TO NEXT CIN

---OUTPUT LCD'S-

U27,U28,U29,U17


=====OR=====

We give the input's to the parallel adder circuit.
For performing the logical operation OR we make the CIN's 1 and the carry obtained at each full adder is the output (since carry=AB + B Cin + A Cin and Cin is 1 so carry=AB + A + B = A + B.)

S6/CONTROL-GROUND
S11-VCC/V
S10-X
S13,S14,S15-VCC

----OUTPUT LCD'S-

U27,U28,U29,U17




