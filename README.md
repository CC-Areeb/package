Follow these steps to setup the project and check the composer.json file for packages
Step 1 - install this composer package for getting the laravel experience when developing your package (personal preferance)
"composer require --dev orchestra/testbench"

If you face the problem of:
PHP Fatal error: Uncaught Error: Call to undefined function each() in D:\xampp\php\pear\PHPUnit\Util\Getopt.php:80 Stack trace: #0 D:\xampp\php\pear\PHPUnit\TextUI\Command.php(242): PHPUnit_Util_Getopt::getopt(Array, 'd:c:hv', Array) #1 D:\xampp\php\pear\PHPUnit\TextUI\Command.php(138): PHPUnit_TextUI_Command->handleArguments(Array) #2 D:\xampp\php\pear\PHPUnit\TextUI\Command.php(129): PHPUnit_TextUI_Command->run(Array, true) #3 D:\xampp\php\phpunit(46): PHPUnit_TextUI_Command::main() #4 {main} thrown in D:\xampp\php\pear\PHPUnit\Util\Getopt.php on line 80

Fatal error: Uncaught Error: Call to undefined function each() in D:\xampp\php\pear\PHPUnit\Util\Getopt.php:80 Stack trace: #0 D:\xampp\php\pear\PHPUnit\TextUI\Command.php(242): PHPUnit_Util_Getopt::getopt(Array, 'd:c:hv', Array) #1 D:\xampp\php\pear\PHPUnit\TextUI\Command.php(138): PHPUnit_TextUI_Command->handleArguments(Array) #2 D:\xampp\php\pear\PHPUnit\TextUI\Command.php(129): PHPUnit_TextUI_Command->run(Array, true) #3 D:\xampp\php\phpunit(46): PHPUnit_TextUI_Command::main()

Then just go inside the file "Getopt.php" and change the " while (list($i, $arg) = each($args)) " with " foreach ($args as $i => $arg) " https://stackoverflow.com/questions/66388326/phpunit-php-fatal-error-uncaught-error-call-to-undefined-function-each

For some odd reason, windows always downloads the oldest phunit version and doesn't know the latest version To solve this issue CAREFULLY FOLLOW THE INSTRUCTIONS PROVIDED IN THE LINK BELOW https://stackoverflow.com/questions/36510071/not-able-to-uninstall-old-version-of-phpunit https://github.com/sebastianbergmann/phpunit

THis is where you can get the exact command for installing phpunit https://phpunit.de/getting-started/phpunit-9.html

Reference video (for windows):- https://www.youtube.com/watch?v=c0cmRy3lhDQ

To execute test cases use the following command:- ./vendor/bin/phpunit

install the parsedown from the following website:- https://parsedown.org/ click on the github if you want to download using composer

To execute the test cases use the following command :- ./vendor/bin/phpunit