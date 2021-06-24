<h1 align="center"> Python Entry Level Programmer Certification </h1>

These notes have prepared based on [Python Entry Level Programmer Certification ](https://beta.kodekloud.com/lessons/introduction-15/).<br /> 

### Print()

+ Built-in function: can be used without importing it.
+ Allows us to print values to the console.
+ We can invoke it with parentheses.
+ We can pass the value we want to print as arguments between the parentheses.
+ The backslash ** \ ** tell python that the next charecter has special meaning (eg. \n)
+ Keyword argument such as **sep** and **end** can be used to format the output

### Literals

A literals use in order to encode data and put them into code.

#### Types

1. Integers
	* Octal Numbers (Starts with 0o)
	* Hexadecimal numbers (Starts with 0x)
2. Floating point numbers
3. Strings
4. Boolean (0-False, 1-True)

### Arithmetic Operators

There are  7 types of operator
| Operator | Description | Example |
|-----|-----|-----|
| + | Adition | x + y |
| -  | Subtraction | x - y |
| \*\ | Multiplication | x * y|
| / | Division (Output may be floating value) | x / y|
| // | Floor Division (Output should be Integers) | x // y |
| % | Modules | x % y|
| \*\*\ | Exponential | x \*\*\ y |

### Variables

+ Variables allow to store values
+ A variables has valid name(letters, digits, underscore, non reserved keyword)
+ Python is dynamically type : variables can be redeclared
+ Can use shortcut operators in order to cleanly redeclare a variable
+ can combine text and variables using **+** operator in print function

### Coments

+ comments allow to add information about code
+ A comment is created by a  # followed by text
+ A multiline comment should have a # infront of every line.

### Input()

+ Prompts the user to input some data from console 
+ It accepts an optional parameter that can be used in order to write <br />
 a message before the user input
+ Alway returns a string.

### String Operations

+ Can use + in order to concatenate two strings
+ Can use \* in order to repeat a string a several amount of times.
+ With the str function, can type-cast a number into string

### Comparision Operators

| Comparision | Descript | Example |
|-----|-----|-----|
| == | Equal to | x == y |
| != | Not equal to | x != y |
| > | Greater than | x > y|
| >= | Greater than and equal to | x >= y|
| < | Lesser than | x < y |
| <= | Lesser than and equal to | x <= y|

### Conditional Statement

+ **If confition** <br />

syntax : 
``` python
		if condition:
			statement
```

+ **If else statement** <br />

Syntax : 
``` python
		if condition:
			statement 1
		else:
			statement 2
```

+ **If then elif else** <br />

Syntax : 
``` python
		if condition 1:
			statement 1
		elif condition 2:
			statement 2
		else:
			statement 3
```

### While loop

The while keyword allow to execute code as long as a certain condition is true

Syntax:		
``` python
		While [ condition ]:
			statement
```

### For loop 

A for loop is used for iterating over a sequence 

Eg:		
``` python
	fruits = ["apple", "banana", "cherry"]
	for x in fruits:
		print(x)
```

### Logical Operator

| Operator | Description |	Example	|
| ------ | ----- | ----- |
| and  |Returns True if both statements are true |x < 5 and  x < 10 |	
| or   |Returns True if one of the statements is true |	x < 5 or x < 4	|
| not  |Reverse the result, returns False if the result is true |	not(x < 5 and x < 10)|

### Bitwise Operator

| Operator |	Name	| Description |
| ------ | ----- | ----- |
| & 	| AND	| Sets each bit to 1 if both bits are 1 |
| \|	| OR	| Sets each bit to 1 if one of two bits is 1 |
| ^	| XOR	| Sets each bit to 1 if only one of two bits is 1 |
| ~ 	| NOT	| Inverts all the bits |
| <<	| Zero fill left shift	|Shift left by pushing zeros in from the right and let the leftmost bits fall off |
| >>	| Signed right shift	|Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off |

### Lists

##### Charecteristic

* Lists items are ordered, changeable and allow duplicate values.
* Lists are created using square brackets.
* The items can be of any data type.
* Elements can be accessed by index and the first item has index [0]
* Elements can also be accessed by Negative indexing, means start from the end and  -1 refers to the last item in the list.
* Lists can be nested to arbitrary depth.

#### Method and Functions in Lists

+ list() - to make a list.
+ len() - The function to find the count of the element in the list
+ sort() - The method to sort the elements in list in ascending order.
+ reverse() - The method tp reverse the element in the list
+ append() - The method to add element to the list
+ insert() - The method to insert the item to desired position
+ extend() - The method to append the element from another list
+ del - to delete the element from list
+ remove() - to remove the specified item from list
+ pop(index_number) - to remove specified index.
+ pop() - to remove last item 
+ clear() - to clear the list
+ To determine if a specified item is present in a list use the **in** keyword <br />
Eg: 
```python
	thislist = ["apple", "banana", "cherry"]
	if "apple" in thislist:
	print("Yes, 'apple' is in the fruits list")
```

### Tuples

##### Charecteristic

* Tuple items are ordered, unchangeable, and allow duplicate values
* Tuples are created using round brackets.
* The items can be of any data type.
* Elements can be accessed by index and the first item has index [0]
* Elements can also be accessed by Negative indexing, means start from the end and  -1 refers to the last item as in lists.

### Dictionary

##### Charecteristic

* A dictionary is a collection which is ordered, changeable and does not allow duplicates.
* Dictionaries are written with curly brackets, and have keys and values
* Elements can be accessed dictionary by referring to its key name, inside square brackets

#### Method and Functions in List

| Methods | Description |
| ----- | ------- |
| dict.clear() | Removes all elements of dictionary dict |
| dict.copy() | copy of dictionary dict |
| dict.keys() | Returns list of dictionary dict's keys |
| dict.values()| Returns list of dictionary dict's values |
| dict.items() | Returns a list of dict's (key, value) tuple pairs |
| dict.popitem() | TO delete the last item  |

### Functions

* A function is a block of code which only runs when it is called.
* We can pass the data to the function called arguments.
* A function can return data as a result.

Syntax :
``` python
		def function_name():
				statement 1
				statement 2
				statement 3
				.
				.
				.
				statement n
				return result
		
		function_name()  # calling function
```

### Quiz

1. print function
2. Literals
3. Arithmetic Operators
4. variables 
5. input function
6. String method 
7. Comparision Operators
8. conditional Statement
9. While loop
10. For loop
11. Logical Operator
12. Bitwise Operator
13. Lists, List Methods, Slicing, Iterating & Nested Lists.
14. Tuples
15. Dictionaries
16. Function arguments, return statement, scopes
