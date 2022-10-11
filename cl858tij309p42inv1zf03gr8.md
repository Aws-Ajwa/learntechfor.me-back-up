# How to Print the Current Date and Time in a PHP Program:

This article will explain the process of how to print the current date and time in PHP. In order to do this, you need to start with a text file and have it ready for printing. This article will also cover the code for printing the current date and time in PHP. If you are interested in learning how to print the current date and time in PHP, then this is the article you should read.

## 1. How to write a PHP program to print the current date and time
Use the PHP date() Function. You can simply use the PHP date() function to get the current date and time in various format, for example, date('d-m-y h:i:s'), date('d/m/y H:i:s'), and so on.
Try out the following example to see how it basically works:
```
<?php
// Return current date from the remote server
$date = date('d-m-y h:i:s');
echo $date;
?>
``` 
The date and time returned by the above example are based on the server's default timezone setting. If you want to show the date and time as per the user's timezone, you can set the timezone manually using the date_default_timezone_set() function before the date() function call.

The following example shows the date and time in the India timezone, which is Asia/Jordan.
```
<?php
// Set the new timezone
date_default_timezone_set('Asia/Jordan');
$date = date('d-m-y h:i:s');
echo $date;
?>
```

## 2. What are the steps to writing a PHP program?

it is really easy steps and they are 

1. Choose a text editor, such as Notepad or Notepad++, and open a new document.
2. Type your PHP code into the document.
3. Save the document as a .php file. For example, you can name it "test.php".
4. Upload the file to your web server.
5. Open the file in your web browser to test it.

## 3. What are the instructions for writing a PHP program?
The instructions for writing a PHP program vary depending on what you want the program to do such as creating a web page or a mobile app. However, some basic instructions for writing a PHP program would be to download a PHP development environment, such as XAMPP, which will give you a local server to test your programs on. Then, create a new file in your development environment and start writing PHP code.

## 4. Wait, What is the difference between a PHP program and PHP code please make it simple?

ok, so A PHP program is a collection of one or more PHP code files that's it.


## 5. How to write a PHP program to print just the time?

```
<?php

$time = date("h:i:sa");

echo "The time is " . $time;

?>
```

## 6. How to write a PHP program to print just the date?

```
<?php

echo date("l, d F Y");

?>
```
## Conclusion: 

You can use the PHP date() function to output the date and time in various formats. The function can take a string that specifies the format of the outputted date and time. We talked about the examples formats and outputs of the current date and time in the article above.
and we will talk later about XAMPP.
thank you for reading.