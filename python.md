# Operators

### Confusing arithmatic operations

+ `/` is the float division
+ `//` is the integer division

### Logical operators

+ `and` is for and
+ `or` is for or
+ `not` is for not

### Confusing comparision operators

Remember `=>` ? I don't know lambda function support in python but `=>` is used for lambda functions.
So it's not the way to write greater than or equal. Surely, the other way.

+ `>=` greater than or equal
+ `<=` less than or equal

### Bitwise operators

| operator | name | description |
| :---: | :---: | :--- |
| & | bitwise and | Bitwise AND |
| \| | bitwise or | Bitwise OR |
| ^ | bitwise xor | Set each bit one only if 2 input bits have different values | 
| ~ | bitwise not | Inverts all the bits |
| << | zero fill left shift | Pushes zeros from the right side. Left most bit false. |
| >> | Signed right shift | Push *copies of left most bit* from left so that the right mose bit fall off. |

## Operator precedence

1. `()`
1. `**`
1. `~ + -` *Note: + and - are urnary + and -*
1. `* / % //`
1. `+ -` addition and substraction
1. `>> <<`
1. `&`
1. `^|`
1. comparision operators(`<=`, `>=`, `>`, `<`)
1. Equality operators (`<>`, `==`, `!=`)
1. Assignment operators ( `=`, `+=`, `-=`, etc.)
1. Identity operators
1. Membership operators
1. Logical operators (`and`, `or`, `not`)

# Data types

*Note : true, false in python starts with caps*
`True` and `False`

+ `str` - string
+ `int`, `float`, `complex` *Note: j represents `sqrt(-1)` so 1j is complex.
+ `list`, `tuple`, `range`
+ `set`, `dict`, `frozenset`
+ `bool`, `bytes`, `bytearray`, `memoryview`

use `type(x)` to get the data type of x.

```
	<class 'range'>
	<class 'int'>
	<class 'float'>
```

### set

`x = {1, 2, 3, "apple"}`

### dict

`x = {"a" : 13, "name" : "jhone"}`

## Slice operator

For lists, it output a list. For strings, output is a string.

`a[1]` returns 1st element of the list. '1st' is zero based.
`a[:]` returns the whole list

`a[i:j]` i will be the index of element where you wanna start. j is the index just before the element you wanna stop.

(+)ve will go from left to right, (-)ve go to the other side.

## Important

`a, b = (2, 3)` is valid. Here, tuple will be shared as a = 2 and b = 3.
