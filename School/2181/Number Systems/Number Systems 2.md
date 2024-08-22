Signed Binary Number Encoding 
 - The leftmost bit ( high-order/most significat bit) indicates whether a number is **Negative** (1) ** or **Non-Negative (0)**
 - Two potential Signed binary encodings
	 - Signed Magnitude 
	 - Two's complement 

Signed Magnitude
 - Treats the high-order bit exclusively as a sign bit 
 - If the high-order bit is 1 then it is negative, and 0 when non-negative
 - The high-order bit does not affect the absolute value of the number

Converting Signed Binary to Decimal 
 - Compute a decimal value for the digits indexed from 0 to (N-2) 
 - Check the (N-1)^th index (most-significant bit). If it's 1, the value is negative, otherwise its non-negative
(1101) = -( 1x2^2 + 0x2^1 + 1x2^0) 
			 = -(1x4 + 0x2 + 1x1) 
			 = -5

Two's Component
 - Treats the high-order bit both as a sign bit and also affects the value of the number
 - if the high-order bit is 1 for an N-bit binary number then (-1x2^N-1) is added to the total sum of all the remaining bits and the number becomes negative
 - if the high-order bit is 0 for a N-bit binay number then (0x2^N-1) is added to the total sum of all the remaining bits and the nubmer becomes positive 

Converting Two's Complement to Decimal 
 - Compute a decimal value for the digits indexed from 0 to (N-2)
 - check the (N-1)^th index (most-significant bit). If it's 1, the value is negative, otherwise it is non-negative 
(1101) = (-1x2^3 + 1x2^2 + 0x2^1 + 1x2^0) 
= (-1x8 + 1x4 + 0x2 + 1x1) 
	= -8 + 4 + 0 + 1
		=-3

Converting Negative Decimal to Two's Complement 
 - Start with decimal in binary 
 - Flip all the bits
 - Add 1
 - Example: to get -13
	 - 0000 1101 (decimal 13)
	 - 1111 0010 ( flip all bits) 
	 - 0000 0001 ( add 1)
	 - 1111 0011 (decimal -13) 

Addition of two unsigned binary numbers 
 - In case of Binary Numbers, each digit holds only 0 or 1 
 - When adding two bits that are both 1, the result carries out to the next digit
 - That means there are also carry ins during the addition of two digits
 - When summing two binary numbers A and B, there are eight possible outcomes depending on the values of DigitA, DigitB, and a CarryIN from the previous digit 
![](Pasted%20image%2020231008205331.png)


Bitwise Operators 
 - AND
 - OR
 - XOR
 - NOT
 - Shifting
	 - Left 
	 - Right

![](Pasted%20image%2020231008210108.png)
![](Pasted%20image%2020231008210125.png)

Bit Shifting 
 - Two types of Bit Shifting
	 - Shifting Left: "<<" is used as the operand 
	 - Shifting Right: ">>" is used as the operand 

Shifting Left
 - Shifting a sequence to the left by N places moves each of its bits to the left N times
 - Appends new zeros to the right size of the sequence
 - Example
	 - 0b 00101101 to the left 2 places
	 - Result: 0b 101101**00**

Shifting Right 
 - Two Variants
	 - Logical Right Shift
		 - Prepends new zeros to the left side (high-order bits) of the sequence
		 - Example: 
			 - Shifting: 0b 10110011 to the right 2 places
			 - Result: 0b **00**101100
	 - Arithmetic Right Shift
		 - Prepends a copy of the shifted value's most significant bit into each of the new bit positions 
		 - Example
			 - Shifting 0b 10110011 to the right 2 places
			 - Result: 0b 11101100




