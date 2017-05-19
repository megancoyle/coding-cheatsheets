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

## Printing
To print items to the screen, use `echo`

## Variables
* Start with a $ followed by a letter or underscore
* Can contain letters, numbers, underscores, or dashes and can't contain spaces
* Case-sensitive
