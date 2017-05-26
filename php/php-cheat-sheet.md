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

## Cookies
* Cookies let us keep track of state for users
* Cookies go in the headers of responses
* Uses `$_Cookie` super global
* `setcookie($name, $value, $expire);`
* Setting cookies must be done before any HTML output unless output buffering is turned on
* End users can find what your cookies are called, so don't use sensitive information there unless it's been encrypted
* To unset a cookie: `setcookie($name, null);` and to tell it to throw away the cookie because it's not useful anymore, use `setcookie($name, $value, (time() - 3600));`

### Sessions
* A session is a file that's stored on the web server
* Have more storage and smaller request sizes than cookies
* Conceal data values
* They are slower to access than cookies
* Designed to expire immediately after user closes their browser
* Session files can accumulate
* PHP handles finding the session for us

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

## Debugging
* Use `<?php phpinfo(); ?>` to access more information about the configurations
* Missing semicolons are a common problem
* To turn on error reporting, in the php.ini file, `display_errors = On` and `error_reporting = E_ALL`, in PHP code, `ini_set('display_errors', 'On');` and `error_reporting(E_ALL);`
* Turn off error reporting on live websites
* Use `echo` to make sure you're getting the right values for variables
* `print_r($array);` to print readable array
* `gettype($variable);` to get variable type
* `var_dump($variable);` to get type and value
* `get_defined_vars();` array of defined variables
* `debug_backtrace();` show backtrace

## Encoding
* For GET requests to pass a reserved character, you must encode them with `urlencode($string)` - letters, numbers, underscores, and dashes will be unchanged, but reserved characters become % + 2-digit hexidecimal, and spaces become +
* For rawurlencode, letters, numbers, and dashes are unchanged, reserved characters become % + 2-digit hexidecimal, and spaces become %20
* Use rawurlencode for the path, before the "?" section, and uses urlencode on the query string
* <, >, &, and " are reserved characters in HTML
* HTML can be encoded with htmlspecialchars() and htmlentities()

## Forms
* Single-page form processing has all logic to the form in one file
* For user-submitted fields, use `htmlspecialchars();` to catch instances when users type in special characters
* For validations, `preg_match()` is useful because you can use regular expressions to check if they're included in the user's input (i.e. '@' and other symbols)
* Use `trim()` to deal with removing spaces for validation

## Functions
* You define a function with the following syntax:
```php
  function name($arg1, $arg2) {
    statement;
  }
```
* You can use letters, numbers, dashes, and underscores, but you can't use spaces.
* Functions must start with a letter or underscore.
* Case insensitive
* Using arrays to return function values, you can use list to assign array values to variables:
```php
  list($result1, $result2) = array_func(10, 5)
  echo "This is result 1: " . $result1 . "<br />";
  echo "This is result 2: " . $result2 . "<br />";
```
* To access global variables in functions, use `global` keyword like with the following: `global $result1;`
* Should use global keyword with caution, since you might change the value of the global variable

## Including and Requiring Files
* `include("file_name.php");`
* Include functions, layout sections (header, footer, etc), reusable HTML/PHP code, CSS and JavaScript
* `require()` does the same thing as `include()` but generates a fatal error if it can't find the file
* `include_once()` keeps an array to the paths it's already included. If it has to include it again, it ignores it since it's already been included
* `require_once()` does the same thing as `include_once()` but for required files

## MySQL and PHP
* You can use mysqli and PDO APIs to connect to MySQL with PHP
* PDO is good to use if you might change to a different database
* To connect to a database: 1) create a database connection, 2) perform database query, 3) use returned data, 4) release returned data, 5) close database connection
* Creating a connection with MySQLi:
```php
    <?php
      $dbhost = "localhost";
      $dbuser = "user_name";
      $dbpass = "password";
      $dbname = "database_name";
      $connection = mysqli_connect($dbhost, $dbuser, $dbpass, $dbname);

      // Test if connection occurred
      if(mysqli_connect_errno()) {
        die("Database connection failed: " .
        mysqli_connect_error() .
        " (" . mysqli_connect_errno() . ")"
      );
      }
    ?>
```
* To end the connection, at the end of the page, add:
```php
  <?php
    mysqli_close($connection);
   ?>
```
* Queries: `mysqli_query()`, for example:
```php
  <?php
  $query = "SELECT * ROW subjects";
  $result = mysqli_query($connection, $query);
  if (!$result) {
    die("Database query failed.");
  }
  ?>
```
* Fetch results: `mysqli_fetch_row()` (fastest way to fetch) or for an associative array, `mysqli_fetch_assoc()` (slightly slower query but gives you a key), or `mysqli_fetch_array` returns in either or both types of arrays (by default it will return both, which makes your memory larger)
```php
  <?php
    while($row = mysqli_fetch_row($result)) {
      // output data from each row
      var_dump($row);
    }
  ?>
```
* Free up memory: `mysqli_free_result()`, with `mysqli_free_result($result);`

## Output Buffering
* `ob_start()`
* `ob_end_flush()`

## Page Redirection
* `header("Location: login.php");`
* add `exit` after the redirect so it doesn't send along any content from the current page

## Printing
To print items to the screen, use `echo`

## Variables
* Start with a $ followed by a letter or underscore
* Can contain letters, numbers, underscores, or dashes and can't contain spaces
* Case-sensitive
