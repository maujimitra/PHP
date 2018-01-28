# PHP's basic functionality

## PHP Basics


### PHP Tags

When PHP parses a file, it looks for opening and closing tags, which are <?php and ?> which tell PHP to start and stop interpreting the code between them. Parsing in this manner allows PHP to be embedded in all sorts of different documents, as everything outside of a pair of opening and closing tags is ignored by the PHP parser.

PHP also allows for short open tag <? (which is discouraged since it is only available if enabled using the short_open_tag php.ini configuration file directive, or if PHP was configured with the --enable-short-tags option).

If a file is pure PHP code, it is preferable to omit the PHP closing tag at the end of the file. This prevents accidental whitespace or new lines being added after the PHP closing tag, which may cause unwanted effects because PHP will start output buffering when there is no intention from the programmer to send any output at that point in the script.

Example

> \<?php

~~~~
echo "Hello world";
// ... more code
echo "Last statement";
the script ends here with no PHP closing tag
~~~~

### Escaping from HTML

Anything you write outside PHP tags that is <?php ?> or <?= ?> will be ignored by PHP

PHP opening and closing tags are:

1. <?php echo 'your string here'; ?>
2. <?= 'your string here' ?> // for PHP 5.4.0 and later
3. <? echo 'this code is within short tags, but will only work '. 'if short_open_tag is enabled'; ?>
4. <script language="php"> echo 'your string here'; </script> // This syntax is removed in PHP 7.0.0.
5. <% echo 'You may optionally use ASP-style tags'; %>
    Code within these tags <%= $variable; %> is a shortcut for this code <% echo $variable; %>
    Both of these syntaxes are removed in PHP 7.0.0.

### Instruction Separation

As in C or Perl, PHP requires instructions to be terminated with a semicolon at the end of each statement. The closing tag of a block of PHP code automatically implies a semicolon; you do not need to have a semicolon terminating the last line of a PHP block. The closing tag for the block will include the immediately trailing newline if one is present.

### Comments

PHP supports 'C', 'C++' and Unix shell-style (Perl style) comments. For example:

* / This is a one-line c++ style comment
* /* This is a multi line comment
    yet another line of comment \*/
* \# This is a one-line shell-style comment

> 'C' style comments end at the first \*/ encountered. Make sure you don't nest 'C' style comments. It is easy to make this mistake if you are trying to comment out a large block of code.

## What PHP supports?

PHP supports ten primitive types.

Four scalar types:

* boolean
* integer
* float (floating-point number, aka double)
* string

Four compound types

* array
* object
* callable
* iterable

And finally two special types:

* resource
* null
