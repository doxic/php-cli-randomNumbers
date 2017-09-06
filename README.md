# PHP CLI Random Numbers

**work in progress**  
Todo:
*



## Introduction

Simple PHP CLI script to guess numbers. Created to teach students basics about PHP (Without any web knowleadge yet)

## Prerequisites

To get a PHP CLI, download [XAMPP](https://www.apachefriends.org/index.html). Install under C:\xampp
Starting commandline with `"C:\xampp\xampp_shell.bat"`

## Random Numbers Script
https://gist.github.com/aknosis/1636629
```PHP
<?php
echo "Are you sure you want to do this?  Type 'yes' to continue: ";
$handle = fopen ("php://stdin","r");
$line = fgets($handle);
if(trim($line) != 'yes'){
    echo "ABORTING!\n";
    exit;
}
echo "\n";
echo "Thank you, continuing...\n";



/**
 * Usage:
 * $answer = prompt("What is your quest?");
 * echo "Answer: $answer";
 * 
 * Outputs:
 * What is your quest?
 * I seek the holy grail!
 * Answer: I seek the holy grail!
 */
function prompt($msg){
	echo "$msg\n";
	return trim(fgets(STDIN));
}
?>
```

## References
* [Read from stdin to a php variable](https://gist.github.com/aknosis/1636629)