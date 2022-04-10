Status:
Tags:
Links: [[Binary]]
___
# Binary Operations
## Addition
- Similar to traditional addition, if the added value is higher than the cap (1), carry it over to the next column
## Subtraction
### Negative values
- Get the cap of the value (2^n-1) and subtract it by the positive binary equivalent of the value, then add it by one 
	- ex) 6 is 0110, so -6 would be 1 + (1111-0110), which would be 1010
## Parts
- 2-bit adders are used to calculate the first column
- 3-bit adders are expandedused to calculate columns with a carry
- 16-bit adders are used to calculate 16-bit numbers
- Consider [[Overflow]]
___
References: