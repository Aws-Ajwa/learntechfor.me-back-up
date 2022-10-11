# basic PHP

## 1. you learned how to make output in [https://learntechfor.me/hello-world](Link)
## 2. Variables: A variable is a value that can be changed in the script.
example of variables:
```
$username = 'johndoe';
$age = 30;
$password = 'secret';
$address = '123 Main Street';
```
## 3. Constants: A constant is a value that cannot be changed in the script. Constants are typically used for configuration values (for example, the database connection string).
example on  Constants:
```
<code>&lt;?PHP

define("MAX_WIDTH", 980);
echo MAX_WIDTH;

?&gt;
</code>
```

## 4. Data types: PHP supports eight primitive types:

Integers
Floats
Strings
Booleans
Arrays
Objects (yes its a data type use google to know more)
Resources
NULL

1.Integers: An integer data type is a non-decimal number between -2,147,483,648 and 2,147,483,647. Rules for integers: An integer must have at least one digit
An integer must not have a decimal point
An integer can be either positive or negative
Integers can be specified in three formats: decimal (10-based), hexadecimal (16-based - prefixed with 0x), or octal (8-based - prefixed with 0)
A decimal integer literal is the default format. This form consists of a sequence of digits without a leading 0 (zero).
```
<code>$x = 1234;  // decimal number
$x = -123;  // a negative number
$x = 0123;  // octal number (equivalent to 83 decimal)
$x = 0x1A;  // hexadecimal number (equivalent to 26 decimal)
$x = 0b11111111; // binary number (equivalent to 255 decimal)
</code>
```
2. Floats: A floating-point number is a number with a decimal point or a number in exponential form. In the following example, $x is a floating-point number.
```
<code>$x = 10.365;
$y = 2.4e3;
$z = 8E-5;
</code>
```
3. Strings: A string is a sequence of characters, like "Hello world!". A string can be specified in four ways:

double quotes
single quotes
heredoc syntax
nowdoc syntax

double quotes:
```
<code>$txt = "Hello world!";
$txt = "John said, \"I am going to work\".";
$txt = 'I am learning PHP at W3Schools.com';
</code>
```
single quotes:
```
<code>$txt = 'Hello world!';
$txt = 'I am learning PHP at W3Schools.com';
</code>
```
heredoc syntax:
```
<code>$str = &lt;&lt;&lt;EOD
//Example of string
//spanning multiple lines
//using heredoc syntax.
EOD;
</code>
```
nowdoc syntax:
```
<code>$str = &lt;&lt;&lt;'EOD'
//Example of string
//spanning multiple lines
//using nowdoc syntax.
EOD;
</code>
```
4.Booleans: A Boolean expresses a truth value. It can be either TRUE or FALSE.

TRUE is often represented by 1
FALSE is often represented by 0

example of boolean:

```
<code>$x = true;
$y = false;
</code>
```

5 . Arrays: An array stores multiple values in one single variable.
In the following example,
 $cars is an array. The index can be assigned automatically (index always starts at 0), or manually:

```
<code>$cars = array("Volvo","BMW","Toyota");
echo "I like ". $cars[0] . ", " . $cars[1] . " and " . $cars[2] . ".";
$cars = array
  (
  array("Volvo",22,18),
  array("BMW",15,13),
  array("Saab",5,2),
  array("Land Rover",17,15)
  );
  
echo $cars[0][0].": In stock: ".$cars[0][1].", sold: ".$cars[0][2].".&lt;br&gt;";
echo $cars[1][0].": In stock: ".$cars[1][1].", sold: ".$cars[1][2].".&lt;br&gt;";
echo $cars[2][0].": In stock: ".$cars[2][1].", sold: ".$cars[2][2].".&lt;br&gt;";
echo $cars[3][0].": In stock: ".$cars[3][1].", sold: ".$cars[3][2].".&lt;br&gt;";
</code>
```

6 . Objects: An object is a data type that stores data and information on how to process that data.
Example of objects:

```<code>&lt;?php
class Car
{
  var $color;
  function Car($color="green") {
    $this-&gt;color = $color;
  }
  function what_color() {
    return $this-&gt;color;
  }
}

function print_vars($obj) {
  foreach (get_object_vars($obj) as $prop =&gt; $val) {
    echo "\t$prop =&gt; $val\n";
  }
}

// Creates one object
$herbie = new Car("white");

// Display the object's properties and values
echo "\herbie: Properties\n";
print_vars($herbie);

?&gt;
</code>```

7 . Resources: A resource is a special variable, holding a reference to an external resource.
Resources are created and used by special functions.
MySQL databases are examples of resources.

8 . NULL: NULL is a special type that only has one value: NULL.
A variable of type NULL is a variable that has no value assigned to it.
Variables can also be emptied by setting the value to NULL:

```<code>&lt;?php
$x = "Hello world!";
$x = null;
var_dump($x);
?&gt;
</code>
```

## 5. Operators: PHP has more than one way to write an if/elseif/else clause and switch.
 For example:
```
// if/elseif/else syntax 
$a = 1; $b = 2; 
if ($a == $b) { echo "a is equal to b"; } 
elseif ($a > $b) { echo "a is greater than b"; } 
else { echo "a is less than b"; } 
// shorthand if/elseif/else syntax 
$a = 1; $b = 2; 
echo ($a == $b) ? "a is equal to b" : ($a > $b) ? "a is greater than b" : "a is less than b";
```

Switch

The switch statement is similar to a series of if statements on the same expression. It is important to end every case with the break keyword. The default keyword is used as the final case.

```
$i = 2; 
switch ($i) { case 0: echo "i equals 0"; 
break; 
case 1: echo "i equals 1"; 
break; 
case 2: echo "i equals 2"; 
break; 
default: echo "i is not equal to 0, 1 or 2"; }
```
## 6. Loops: do...while / while/for/foreach/- loops 
do...while loop through a block of code as long as the condition specified in the while statement is true.
example on do...while Loops:
```
<code>&lt;?php
$x = 1; 

do {
    echo "The number is: $x &lt;br&gt;";
    $x++;
} while ($x &lt;= 5);
?&gt; 
</code>```

While

A while loop will execute a block of code if and as long as a specified condition is true.

```
$i = 1; 
while ($i <= 10) { echo $i++; /* the printed value would be 
// $i before the increment
// (post-increment) */ } 
$i = 1; while ($i <= 10): echo $i; 
$i++; endwhile;
```
For

The for loop is used when you know in advance how many times the script should run.

```
for ($i = 1; $i <= 10; $i++) { echo $i; }
 // shorthand for loop echo '1-10: ';
 for ($i = 1; $i <= 10; 
echo $i, $i++ < 10 ? ', ' : ' ');
```
Foreach

The foreach loop works only on arrays, and it is used to loop through each key/value pair in an array.

```
$arr = array(1, 2, 3, 4); 
foreach ($arr as &$value) { $value = $value * 2; }
 // $arr is now array(2, 4, 6, 8) 
// foreach by reference 
$arr = array("one", "two", "three"); 
foreach ($arr as $value) { echo $value . "<br />"; }
```

## 7. Functions: A function is a block of statements that can be used repeatedly in a program. A function will not execute immediately when a page loads. A function will be executed by a call to the function.
example of Functions:

```<code>&lt;?php
function writeMsg() {
    echo "Hello world!";
}

writeMsg(); // call the function
?&gt; 
</code>``` 

 **but these are just the basic things that you should learn on PHP**

# conclusion:
I hope you enjoyed this post and I think this post is helpful to you.
so please share this with your friends and 
you're family because sharing is caring.
Next time we will talk more about php.