# PHP-SYNTAX-GUIDE
12 PHP Syntax Categories with Examples

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

Variables are used to store data, like a number or string of text. They start with **$** and contains only numbers, letters and underscores ( **\_** ), no spaces. Also, the variable cannot start with a number. Variables can be declared without a value assigned, as it can be defined later, or redefined. List the variable first, then use the **=** assignment operator, followed by the value and finished off with a semicolon. Laslty, variables are case sensitive, so **$example** is different from **$Example**.

```
$your_variable = your value goes here;
$_your_variable1 = 1000;
```
   
