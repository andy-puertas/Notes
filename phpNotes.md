### PHP NOTES

*****

#### PHP


`$` signifies an object that stores data.
* cannot start with numbers
* case sensitive
* white space doesn't affect code
* there is a difference between single and double quotes

********
##### Escapes

* `\"` print as double quote, not string closer
* `\n` print a new line
* `\t` tab character
*****

##### Variable Types
* integer
* floating point
* string
* array
* object
* resource

*****

##### Comments

* `//`
* `#`
* `/* */` these cannot be nested


*****

##### Conditional Statements

`if (    ) {
     
} else {}


braces are not necessaray if it is on the same line.

```php
<?php
    $Name = 'Bob';
    switch($Name) {
        case "Jim": print "Your name is Jim\n"; break;
        case "Linda": print "Your name is Linda\n"; break;
        case "Bob": print "Your name is Bob\n"; break;
        case "Sally": print "Your name is Sally\n"; break;
        default: print "I do not know your name!\n";
    }
?>
```

notice the break.  that keeps the code from continuing

*****

##### Loops


* `while (condition is true) {
    do code
}`

 A for loop has three parts - a declaration, a condition, and an action

```php
<?php
    for ($i = 1; $i < 10; $i = $i + 1) {
        print "Number $i\n";
    }
?>
```
