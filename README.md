# PHP SYNTAX GUIDE - 12 PHP Syntax Categories with Examples

A general note, all lines of code need to end with a semicolon or your webpage will not load and you will see a "HTTP Error 500".

## PHP Single & Multi-line Comments

**Single line comments** are similar to Javascript, just put **//** or **#** before the comment or line of code you don't want to be run.

```
<?php

// This is a single line comment
# This is also a a single line comment

?>
```

**Multi-line comments** are the same as CSS and JS, just put **/*** before the lines of code or comment and add ***/** to the end.

```
/* This is a multi-line comment,
   which can also be used to prevent
   a block of code from being run */
```
   
## PHP Variables

**Variables** are used to store data, like a number or string of text. They start with **$** and contains only numbers, letters and underscores **\_**, no spaces. Also, the variable cannot start with a number. Variables can be declared without a value assigned, as it can be defined later, or redefined. List the variable first, then use the **=** assignment operator, followed by the value and finished off with a semicolon. Laslty, variables are case sensitive, so **$example** is different from **$Example**.

```
$your_variable = "your value goes here";
$_your_variable1 = 1000;
```

## PHP Constants

**Constants** are similar to variables, but as the names differ, the functions also differ. Constants will not be accidently changed once they're defined.

```
define("company_email", "contact_us@company.com"); // this defines the constant
 
echo 'Please send comments and suggestions to: ' . company_email; // prints Please send comments and suggestions to: contact_us@company.com
```

## PHP Echo and Print Statements

The **echo** statement will display the value of a variable or html code.

```
echo $your_variable; //displays the text: your value goes here
echo  "<h1>Example Header</h1>"; //displays the text "Example Header" with the h1 header style. 
```

The **print** statement will write whatever text you put in quotes or html markup. It is very simialr to the echo statement, but can only print one string.

```
print "your text goes here"; //displays the text: your text goes here
print "<h1>Example Header</h1>"; //displays the text "Example Header" with the h1 header style. 
```

## PHP Data Types

### Integers

There is 5 types of **integers** that PHP can process; decimal, negative, hexagonal, octal and binary numbers.

```
$a = 123; // decimal number
var_dump($a); // prints int(123)
 
$b = -123; // a negative number
var_dump($b); // prints int(-123)
 
$c = 0x7B; // hexadecimal number
var_dump($c); // prints int(123)
 
$d = 0173; // octal number
var_dump($d); // prints int(123)
$e = 0b1111011; // binary number
var_dump($e); // prints int(123)
```

### PHP Strings

A **string** is a group of characters, including spaces. A string can contain up to 2147483647 characters(or 2GB). They start and end with matching single quotes or double quotes. You can use a backslash \ (escape character) in front of an of a single or double quote to display it as a character rather than ending the string.

```
$single = 'Single Quotes';
echo $single; // prints Single Quotes
  
$double = "Double Quotes";
echo $double; // prints Double Quotes
  
$escape = 'I\'m not 6\' tall';
echo $escape; // prints I'm not 6' tall 
```
  
### PHP Floating Point Numbers
  
**Floating point numbers**, also refered to as as **'doubles'** or **'real numbers'**, are decimal or fractional numbers.
  
```
$a = 20.202;
var_dump($a); // prints float(20.202)

 
$b = 10.5e5;
var_dump($b);  // prints float(1050000)

$c = 3E-10;
var_dump($c); // prints float(3.0E-10)
```

## PHP Booleans

**Booleans** are either on or off, 1/true or 0/false.

```
$boolean_1 = True;
var_dump($boolean_1); // prints bool(true)

$boolean_0 = False;
var_dump($boolean_0); // prints bool(false)
```

## PHP Arrays

### Multidimensional Arrays

**Arrays** are complex variables, that can hold multiple values and can even have arrays within the array(**multidimensional arrays**).  
```
$employee_email = array(
    array(
        "name" => "Fred Smith",
        "email" => "fsmith@company.com",
    ),
    array(
        "name" => "John Davidson",
        "email" => "jdavidson@company.com",
    ),
    array(
        "name" => "Andrew Tasker",
        "email" => "atasker@company.com",
    )
);
echo "John Davidson's company email is: " . $employee_email[1]["email"]; // a nested value in a multidimensional array prints John Davidson's company email is: jdavidson@company.com
```
### Indexed Arrays

**Indexed arrays**, the values have an numbered index starting from 0.

```
$employees = array("Fred Smith", "John Davidson", "Andrew Tasker");
print_r($employees); // indexed array prints  Array ( [0] => Fred Smith [1] => John Davidson [2] => Andrew Tasker )
```
### Associated Arrays

**Associated arrays** have a named key instead of a number. These can be very useful to store data about a particualr value.

```
$employees_position = array(
    "Fred Smith" => "General Manager",
    "John Davidson" => "Production Supervisor",
    "Andrew Tasker" => "Clerk"
);
print_r($employees_position); // associated array prints Array ( [Fred Smith] => General Manager [John Davidson] => Production Supervisor [Andrew Tasker] => Clerk )
```
## PHP Operators

**Operators** are special characters that can be singular or combined to do arithmetic, comparisons and other similar functions.

### Arithmetic Operators

These operators are pretty common in other scripting languages:

"+" addition, "-" subtraction, "\*" multiplication, "/" division and "%" modulus.

```
// modulus example (remainder from a division equation)
$a = 7;
$b = 3;
echo($a % $b); // the modulus would be 1
```

### Assignment Operators

**Assignment Operators** can shorten a equation to assign a value to a variable, or simply just assign a value with **"="**.

```
+=	| Add and assign             | $a += $b |	$a = $a + $b,
-=	| Subtract and assign	     | $a -= $b | $a = $a - $b,
*= | Multiply and assign	     | $a *= $b |	$a = $a * $b,
=	| Divide and assign quotient | $a /= $b |	$a = $a / $b,
%=	| Divide and assign modulus  | $a %= $b |	$a = $a % $b,
```

```
$a = 7;
$a += 13;
echo $a; // prints 20
```

### Comparison Operators

**Comparison operators** compare two values in a with True or False(boolean).

```
==  |	Equal	                   | $x == $y  | True if $x is equal to $y,
=== |	Identical	             | $x === $y |	True if $x is equal to $y, and they are of the same type,
!=	 | Not equal	             | $x != $y	 | True if $x is not equal to $y,
<>	 | Not equal	             | $x <> $y	 | True if $x is not equal to $y,
!== |	Not identical	          | $x !== $y | True if $x is not equal to $y, or they are not of the same type,
<	 | Less than	             | $x < $y	 | True if $x is less than $y,
>	 | Greater than	          | $x > $y	 | True if $x is greater than $y,
>=	 | Greater than or equal to |	$x >= $y	 | True if $x is greater than or equal to $y,
<=	 | Less than or equal to	 | $x <= $y	 | True if $x is less than or equal to $y,
```

```
$a = BIG;
$b = big;
var_dump($a === $b); prints bool(false), because one variable is uppercase and the other is lowercase.

$a = BIG;
$b = big;
var_dump($a !== $b); prints bool(true), because they are equal, but not identical.
```

### Incrementing and Decrementing Operators

These operators increment/decrement a variable's value.

```
++$x	| Pre-increment	| Increments $x by one, then returns $x,
$x++	| Post-increment	| Returns $x, then increments $x by one,
--$x	| Pre-decrement	| Decrements $x by one, then returns $x,
$x--	| Post-decrement	| Returns $x, then decrements $x by one,
```

```
$x = 9;
echo $x++; // returns 9, but the next time the variable echoed the increment will be present.
echo $x;   // returns 10
```

### Logical Operators

**Logical operators** can be used to combine conditional statements.

```
and | And | $x and $y | True if both $x and $y are true,
or  | Or	 | $x or $y  | True if either $x or $y is true,
xor | Xor | $x xor $y | True if either $x or $y is true, but not both,
&&	 | And | $x && $y  | True if both $x and $y are true,
||	 | Or	 | $x || $y  | True if either $$x or $y is true,
!   | Not | !$x       | True if $x is not true,
```

```
$age = 15;
// a youth for this example is 13-17
if(($age > 12) || ($age < 18)){
    echo "$age is a youth.";
} else{
    echo "$year is not a youth.";
} // prints 15 is a you
```

### String Operators

The is 2 **string operator**, "." will join the variables together(concantenate), ".=" will append the second value to the first variable, so the first variable is reassigned as a combination of the 2.

```
$a = "Thank";
$b = " you";
echo $a . $b; // prints Thank you
 
$a .= $b;
echo $a; // prints Thank you
```

### Array Operators

**Aarray operators** are basically comparison operators for arrays, with the addition of **union**.

```
+	 | Union	       | $x + $y	 | Union of $x and $y,
==	 | Equality	    | $x == $y	 | True if $x and $y have the same key/value pairs,
=== | Identity	    | $x === $y | True if $x and $y have the same key/value pairs in the same order and of the same types,
!=	 | Inequality	 | $x != $y	 | True if $x is not equal to $y,
<>	 | Inequality	 | $x <> $y	 | True if $x is not equal to $y,
!== | Non-identity | $x !== $y | True if $x is not identical to $y,
```
