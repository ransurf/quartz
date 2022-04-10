---
aliases:
---
Status:
Tags: #aCards/cmpt295/binary 
Links: [[Binary Float Byte Structure]]
___

# IEEE Float Representation

## Principles
[![Image from Gyazo](https://i.gyazo.com/4769174de634bf760cad5a0a43bb5b83.png)](https://gyazo.com/4769174de634bf760cad5a0a43bb5b83)

Format
?
[![Image from Gyazo](https://i.gyazo.com/a54bbe9f776cb006987cb7be29ac6dc8.png)](https://gyazo.com/a54bbe9f776cb006987cb7be29ac6dc8)
- signed bit
<!--SR:!2022-03-23,3,130-->

### Steps
?
1. Find binary equivalent of number through /2 method
- Bottom to top for int
- Top to bottom for fractional
2. Move decimal to right of leading 1, find scientific notation
- Positive if you have to go right to go back to original
- Mantissa (M) = exponent
3. Find bias
- Add 127, convert to binary
4. Remove leading 1, round mantissa up or down
<!--SR:!2022-04-05,19,130-->

## Form
?
Binary numerical form ;; $V = (-1)^s M2^E$
<!--SR:!2022-03-23,3,130-->

Calculating E, bias, M, normalized
?
- S is signed bit
- Exponent shifts decimal, is not multiplied by $2^E$
- **E =** exp - bias
	- *ex) if exp = 001 and bias = 3, then 1 - 3 = -2*
		-  *(E for 6-bit representation)*
- **bias =** $2^{k-1} - 1$
	- *ex) if k=2 (6-bit representation), bias would be 4-1 = 3*
- **M =** 1 + frac
	- *ex) 1.frac*
<!--SR:!2022-03-21,1,131-->

Calculating E, bias, M, denormalized
?
- **E =** 1 - bias
	- *ex) 1 - 3 = -2, E for 6-bit representation
- **bias =** $2^{k-1} - 1$
	- *ex) if k=2 (6-bit representation), bias would be 4-1 = 3*
- **M =** frac
	- *ex) .frac*
<!--SR:!2022-03-22,1,130-->

- Move decimal to left most 1, count number of movements
	- Movements is unbiassed exponent
	- Resulting number is mantissa
- Determine biased exponent
	- add 127 to unbiased, then conver to integer
	[![Image from Gyazo](https://i.gyazo.com/9cbf8c44d7c819c5f44e0fbb59d3930f.png)](https://gyazo.com/9cbf8c44d7c819c5f44e0fbb59d3930f)zz
- Remove leading 1 from mantissa
	- 1 is always real, so no need to store
	- pad with 0's

### Float
?
[![Image from Gyazo](https://i.gyazo.com/f930f3c87cdc678f6895a8fac6d20bff.png)](https://gyazo.com/f930f3c87cdc678f6895a8fac6d20bff)
<!--SR:!2022-04-07,21,130-->

#### Special Cases (all 0/1)
?
[![Image from Gyazo](https://i.gyazo.com/c82b207423f32e564cead41b8fbf29af.png)](https://gyazo.com/c82b207423f32e564cead41b8fbf29af)
<!--SR:!2022-03-23,3,130-->

### Double
[![Image from Gyazo](https://i.gyazo.com/c096693158cca0cb5351c011f9af736c.png)](https://gyazo.com/c096693158cca0cb5351c011f9af736c)

## Examples
Convert
2. Conver to pure binary
	- Multiply by 2, mod 1 for binary value
	- Keep going until 0
	- Read top to bottom

### Convert Decimal to IEEE
Convert 0.09375 to ieee
?
[![Image from Gyazo](https://i.gyazo.com/90f7a4befbbdeb1504fbe9613d80cfcf.png)](https://gyazo.com/90f7a4befbbdeb1504fbe9613d80cfcf)
- When you notice that the dividend was previously encountered, it means a repeating number
<!--SR:!2022-03-22,1,130-->

Convert -123.3
?
[![Image from Gyazo](https://i.gyazo.com/54238a27a57f46ec62f112ab7e93a884.png)](https://gyazo.com/54238a27a57f46ec62f112ab7e93a884)
<!--SR:!2022-04-06,20,130-->

### Convert IEEE to Decimal
[![Image from Gyazo](https://i.gyazo.com/67a743fea547a35871ef1df8c04cb2d5.png)](https://gyazo.com/67a743fea547a35871ef1df8c04cb2d5)
?
[![Image from Gyazo](https://i.gyazo.com/d924d9b79e05016c9ecbf56b038a3340.png)](https://gyazo.com/d924d9b79e05016c9ecbf56b038a3340)
<!--SR:!2022-04-09,23,150-->

[![Image from Gyazo](https://i.gyazo.com/a6f8825867641c4388b7cdc8536f400b.png)](https://gyazo.com/a6f8825867641c4388b7cdc8536f400b)
?
[![Image from Gyazo](https://i.gyazo.com/a9f0a92b7d439fefa5993b23eb340f07.png)](https://gyazo.com/a9f0a92b7d439fefa5993b23eb340f07)
___
<!--SR:!2022-04-04,18,130-->

# Backlinks
```dataview
list from [[IEEE Float Representation]] AND !outgoing([[IEEE Float Representation]])
```
___
References:

Created:: 2022-01-21 14:51
