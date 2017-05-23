# PHP: Overview
PHP is an open-source, server-side scripting language.

## Comments
```php
  <php?
  // this is a single-line comment
  # this is another way to make a single-line comment

  /* multi-line comments are written like
  this so you can keep writing more lines */
  ?>
```

## Data Types

### Arrays
* To create a variable and assign it to an empty array, use the following format: `$newarr = array();`
* To create a variable and assign it to an array, use: `$newarr = array(3,5,6,22,16,30);`
* `<?php echo print_r($newarr); ?>` use `print_r` or print readable when working with arrays to see their contents
* Shorter notation (which works with newer versions of php): `$newarr = [2,3,6,8,10];`

### Associative Array
* An object-indexed collection of objects
* Used when you need a key to retrieve data
* `echo $newarr[1]` wouldn't work unless assign keys with indexes for an associative array

#### Array pointers
* `current($array);` current pointer value in array
* `next($array);` move the pointer forward
* `prev($array);` move the pointer backward

### Array Functions
* `count($newarr);` to tell how many items are in an array
* `max($newarr);` tells the maximum value in the array
* `min($newarr);` tells the minimum value in the array
* `sort($newarr);` sorts the array in ascending value (for strings, word sort in alphabetical order)
* `rsort($newarr);` sorts the array in descending order
* `implode(" * ", $newarr);` turns array into a string, first argument is how to separate each array item
* `explode(" * ", $newarr);` first argument tells it where to separate each item, turns a string into an array
* `in_array(5, $newarr);` for finding if something exists in an array - first argument is the item you're looking for

### Constants
* The value of constants doesn't change
* `define("CONST_VALUE", 50);`
* Use quotes when defining the constant, once it's been defined, don't use the quotes when referencing it
* Can't redefine them

### Booleans
* When it outputs true into a string, it outputs 1. For false, it outputs nothing.
* `is_bool();` for checking if a variable is a boolean
* True and False can be written in uppercase or lowercase

### Floats
* An example of a float is `1.55`
* You can divide integers to get floating point numbers
* `round(number1, number2)` takes a number and how many significant digits you want there to be
* `ceil(number)` ceiling always rounds up
* `floor(number)` floor always rounds down
* `is_float(number)` to determine whether something is a float

### Functions
* `strtolower()` changes a string to lower-case
* `strtoupper()` changes a string to upper-case
* `ucfirst()` changes first letter in string to upper-case
* `ucwords()` changes first letter of every word in the string to upper-case
* `strleng()` finds length of the string
* `trim()` eliminates white spaces
* `strstr()` find a string within a string (pass two parameters). Find a string within a string
* `str_replace()` takes three parameters - the string you're looking for, what you want to replace it with, and the item we're searching in

### Integers
* `abs(0 - 100)` absolute value
* `pow(3, 6)` exponential (first number to the power of the second number)
* `sqrt(25)` square root
* `fmod(17, 3)` modulo
* `rand()` random
* `rand(1,20)` random (min, max)
* `is_int(number)` to determine whether something is an integer

### Null and empty
* Case insensitive
* `is_null();` will test if an item is null
* An empty string, null, 0, 0.0, "0", false, and an empty array, are all considered items that are empty

### Strings
* Strings can include letters, text, html.
* Use double quotes or single quotes to denote strings
* Can do variable replacement inside of a string (but only when you use double quotes):
```php
  <?php
  $phrase = "Hello World";
  ?>

  <?php
    echo "$phrase printed here<br>";
  ?>
```
* For in place substitution, use `echo "{$phrase} Here<br>";`

### Type Juggling and Casting
* When PHP converts a value from one type to another for us on the fly, it's called type juggling.
* When we explicitly set a type ourselves, it's called type casting.
* To set type can use `settype($variable, "integer")` or `(integer) $variable`
* The types we can use are string, int or integer, float, array, bool or boolean
* `gettype();` best way to figure out the value type

## Printing
To print items to the screen, use `echo`

## Variables
* Start with a $ followed by a letter or underscore
* Can contain letters, numbers, underscores, or dashes and can't contain spaces
* Case-sensitive
