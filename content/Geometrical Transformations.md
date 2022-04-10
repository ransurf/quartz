---
aliases:
---
Status:
Tags: #cards/math232/unit3
Links: [[Transformations]]
___

# Geometrical Transformations

## Principles
if tx=ty
- Dilation is when ty>1
- Contraction is when ty<1

### Types

#### Rotation about origin
Linear transformation:
[![Image from Gyazo](https://i.gyazo.com/ba7c34ea729293347c56552461aa325f.png)](https://gyazo.com/ba7c34ea729293347c56552461aa325f)
When applied to standard basis vectors, we get the f ollowing
[![Image from Gyazo](https://i.gyazo.com/f494cf93c51f32df5fa664c6ebd7472e.png)](https://gyazo.com/f494cf93c51f32df5fa664c6ebd7472e)
- $R_o$ can be multiplied to another vector to find its new position after rotation

#### Stretching in x or y direction
X
- [![Image from Gyazo](https://i.gyazo.com/7dc9b95588f27686c9617ae8e72eb206.png)](https://gyazo.com/7dc9b95588f27686c9617ae8e72eb206)
- Use basis vectors to exemplify effects

Y
- [![Image from Gyazo](https://i.gyazo.com/aaf293133246a5582446cf61095a8bcb.png)](https://gyazo.com/aaf293133246a5582446cf61095a8bcb)

#### Shear
Horizontal Shear
- [![Image from Gyazo](https://i.gyazo.com/6f46107cac6f3bd891aefc13e01addae.png)](https://gyazo.com/6f46107cac6f3bd891aefc13e01addae)
- Take first component + s(2nd component)
- Can create paralellogram, idk why

#### Reflection through origin
[![Image from Gyazo](https://i.gyazo.com/0cacc1b3d05693443d70467f2b9ca3fd.png)](https://gyazo.com/0cacc1b3d05693443d70467f2b9ca3fd)

#### Reflection through line instersecting origin
[![Image from Gyazo](https://i.gyazo.com/8310ebf3066d06ec558eec6f0c58224d.png)](https://gyazo.com/8310ebf3066d06ec558eec6f0c58224d)

Just confused on how perp = proj? Other than that makes sense
- Parametric (green) found by setting x2= something and finding x1 by moving x2 to RHS
- Identity matrix is just i-2proj since the transformation is just

Procedure
?
- If given linear equation, convert to scalar and plot
- Find vector and normal through the leading variables
	- Vector is slope of y intercept form, y/x
- Find projection of standard basis vectors with n as subscript
- Input into a' equation, identity matrix - combined proj
- 
___
<!--SR:!2022-03-04,1,130-->

# Backlinks
```dataview
list from [[Geometrical Transformations]] AND !outgoing([[Geometrical Transformations]])
```
___
References:

Created:: 2022-01-30 16:54
