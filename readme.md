# Basic Coding Standards

Note: I created this repository at the request of my dear colleagues. The language which is used in examples is PHP, but it's suitable for everyone and could be used in almost all modern programming languages.

This repo represents basic coding standards that could be found in PSR 0,1,2

## Classes

Class names should be in studly case format:

Examples:

```php
class MyPaperBook {} // correct
class myPaperBook {} // wrong
class my_paper_book {} // wrong
```



## Methods

Methods should be in camel case format:

Examples:

```php
class MyPaperBook 
{    
    public function getMyBook() {}   // correct
    public function GetMyBook() {}   // wrong
    public function get_my_book() {} // wrong
}
```



## Properties

Class properties should be in camel case format:

Examples:

```php
class MyPaperBook
{
    protected $bookName  = ''; // Correct
    protected $book_name = ''; // wrong
    protected $BookName  = ''; // wrong
}
```



## Constants

Class constants should be in uppercase format:

Examples:

```php
class MyPaperBook
{
    const PRICE = 10000; // correct
    const PRICE_UNIT = 2; // correct
    const price = 4000; // wrong
}
```



## Variables

Variables do not obey a restricted standard

```php
$book_name = 'Hello world'; // correct
$bookName = 'Hello world';  // correct
```



## Internal keywords and True/False/Null ()

All internal keywords plus true, false and null should be in lowercase format:

```php
$var = true; // correct
$var = TRUE; // wrong

$var = null; // correct
$var = NULL; // wrong
```



## Line length

Lines length should be between 80 and 120 characters. If it exceeded, you should break the line at an appropriate position

```php
class MyPaperBook
{

    // Long method name and args decreases readability
    public function getMyBookFromDatabase(string $bookName, array $cols = ['id', 'name'], integer $limit = 10) {
     	// ...   
    }
    
    // The corrected style
    public function getMyBookFromDatabase(
        string $bookName,
        array $cols = ['id', 'name'],
        integer $limit = 10
    ) {
     	// ...   
    }
    
    protected $array = [
        'one',
        'two',
        'three',
        'four',
        'five',
        'six',
        'seven',
        'eight',
        'nine',
        'ten',
    ];
}
```



## Intenting

Use 4 spaces for intentings. Do not use tabs.



## Method Arguments

See the argument list, There must be a space after each comma:

```php
function foo($arg1, $arg2, $arg, ...) {}; // correct
function foo($arg1,$arg2,$arg, ...) {}; // wrong
```



## Conditions, Loops ...

Example:

```php
// Correct form
if (condition) {
    
} else if (condition) {
    
} else {
    
}

// Wrong forms:

// No space before opening parenthesis and after closing parenthesis
// else must be right after `if` closing bracket

if(condition){ 
    
}
else { 
    
}


// Correct form: Space before opening parenthesis and after closing parenthesis
for ($i = 0; $i < 5; $i++) {
    
}

// Try catch is similar to if else. Look catches' placement
try {
    
} catch (Exception $e) {
    
} catch (Exception $e) {
    
}



switch ($var) {
    case 'a':
        $bar = 2;
        break; // Correct placement of `break`
    case 'b':
        $bar = 1;
    break; // Wrong placement of `break`. One missing intent. Because break is part of `case` body
}
```



## Acronyms

HTML, NASA, XML, IDE ...

```php
$html; // correct
$HTML; // wrong
$Html; // wrong

$hackNasa; // correct
$hackNASAWithHTML; // wrong

```



