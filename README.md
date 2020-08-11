# 8bitBoothMultiplier
Booth Multiplication using Verilog that multiplies two signed binary number in two’s complement notation.

Booth algorithm gives a procedure for multiplying binary integers in signed 2’s complement representation in efficient way, i.e., less number of additions/subtractions required. It operates on the fact that strings of 0’s in the multiplier require no addition but just shifting and a string of 1’s in the multiplier from bit weight 2^k to weight 2^m can be treated as 2^(k+1 ) to 2^m.

As in all multiplication schemes, booth algorithm requires examination of the multiplier bits and shifting of the partial product. Prior to the shifting, the multiplicand may be added to the partial product, subtracted from the partial product, or left unchanged according to following rules:

The multiplicand is subtracted from the partial product upon encountering the first least significant 1 in a string of 1’s in the multiplier The multiplicand is added to the partial product upon encountering the first 0 (provided that there was a previous ‘1’) in a string of 0’s in the multiplier. The partial product does not change when the multiplier bit is identical to the previous multiplier bit.

###### Procedure to do the multiplication manually
1.	Take M as multiplicand.
2.	Take Q as multiplier.
3.	Consider a 1-bit register Q-1which is initialized to 0.
4.	Consider a register A which is initialised to 0.


###### Conditions
1.	If Q0Q-1 are either 00 or 11 then, perform arithmetic right shift by 1 bit.
2.	If Q0Q-1=10 then perform A←A-M
And then perform arithmetic right shift.
3.	If Q0Q-1=01 then perform A←A+M
And then perform arithmetic right shift.

**Booth’s algorithm calculates the product in n steps where n is the number of bits used to represent the numbers.**
