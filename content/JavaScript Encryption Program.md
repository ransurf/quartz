Status:
Tags: #js 
Links: [[JavaScript MOC]]
___
# JavaScript Encryption Program
- [[Caesar Cipher]]
## Design (Back-End)
### Classes
#### ConversionInstance
> Stores some information of the current conversion
##### Properties
- `id`
- `input`
- `conversionType`
- `output`
##### Methods
- `log`
	- Logs the instance into array for previous actions
#### Encryption/Decryption Methods
> Have objects for the different kinds of encryptions/decryptions
> **ex)** `Enigma` or `CaesarShift`
> Refer to [[Encryption Methods Implementation]]
##### Properties
- `toEncrypt`
	- true if user wants encryption, false otherwise
- Appropriate values needed for performing the conversion
	- Grabbed from the user input
	- Variable depending on the kind of conversion
##### Methods
- `setProperties`
	- Sets the properties of the conversion that is going to happen
	- Pulls values from user input fields
- `encrypt`
	- Takes `ConversionInstance`
	- Manipulates 
- `decrypt`
#### Log
> Stores previous conversions
##### Properties
- `previousConversions`
##### Methods
- `getConversion`
	- Fills input fields of previous conversion
### Functions
#### Runner function (onClick)
- Creates a new `Conversion` object
- Checks whether encryption or decryption
- Switch statements to find out which encryption/decryption needs to be done
- Performs conversion
	- ex) If the user wanted an `Enigma` encryption:
		1. `Enigma.setProperties();`
		2. `ConversionInstance.setOutput( Enigma.encrypt() );`
- Stores object conversion through `ConversionInstance.log();`
- Program LMAO
___
References:

Created:: 2021-05-31 18:50 PM