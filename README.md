# PHP-SYNTAX-GUIDE

##12 PHP Syntax Categories with Examples

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

Variables are used to store data, like a number or string of text. They start with **$** and contains only numbers, letters and underscores **\_**, no spaces. Also, the variable cannot start with a number. Variables can be declared without a value assigned, as it can be defined later, or redefined. List the variable first, then use the **=** assignment operator, followed by the value and finished off with a semicolon. Laslty, variables are case sensitive, so **$example** is different from **$Example**.

```
$your_variable = "your value goes here";
$_your_variable1 = 1000;
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

There is 5 types of integers that PHP can process; decimal, negative, hexagonal, octal and binary numbers.

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

A string is a group of characters, including spaces. A string can contain up to 2147483647 characters(or 2GB). They start and end with matching single quotes or double quotes. You can use a backslash \ (escape character) in front of an of a single or double quote to display it as a character rather than ending the string.

```
$single = 'Single quotes';
echo $single;
  
$double = "Double Quotes";
echo $double;
  
$escape = 'I\'m not 6\' tall';
echo $escape;
  
```
  
### PHP Floating Point Numbers
  
Floating point numbers, also refered to as as 'doubles' or 'real numbers', are decimal or fractional numbers.
  
```
$a = 20.202;
var_dump($a); // prints float(20.202)

 
$b = 10.5e5;
var_dump($b);  // prints float(1050000)

$c = 3E-10;
var_dump($c); // prints float(3.0E-10)
```
  
   
