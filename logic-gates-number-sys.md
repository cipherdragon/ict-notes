# Number systems

## Converting a 2's complement number to decimal

Identify the sign of the final decimal number by MSB(most significant bit).

+ MSB 0: (+)ve 
+ MSB 1: (-)ve

### (+)ve decimal

Just convert the binary to decimal.

### (-)ve decimal 

1. Get the binary number.
1. Invert the bits
1. Add 1 to the LSB.
1. Convert the number to decimal.
1. Take sign of the decimal number as (-)ve.

## Converting a decimal to 2's complement

1. If it's a (+)ve, just convert to binary, else,
1. Consider only the numerical value of the decimal.
1. Invert the bits and add 1 to the LSB.

<br />

1. +5 is 00000101 in 8 bits. 
1. Invert the bits -> 11111010
1. Add one -> 11111011
1. 2's complement -5 in 8 bit binary is 11111101

## One's complement

+ convert (+) decimals as it is.
+ For (-)ve, convert to binary considering just the numerical part and flip bits.

## Sign magnitude

A 8 bit binary system that uses the MSB to represent the sign of the number. Conventionally,
0 for MSB represent a (+)ve, otherwise for a (-)ve. Other 7 bits is used to represent the 
actual number

+ This method allows to have both +0 and -0.

## Common usage of 1's complement, 2's complement and Sign Magnitude 

| system         | Usage                                                                        |
|----------------|------------------------------------------------------------------------------|
| 1's complement | Simpler design in hardware                                                   |
| 2's complement | Can be used to build low cost, high speed hardware for arithmetic operations |
| Sign Magnitude | Cannot used to add or subtract, used in analogue --> digital conversion      |
