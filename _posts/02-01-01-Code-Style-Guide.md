---
anchor: code_style_guide
---

# Code Style Guide  {#code_style_guide_title}

The PHP community is large and diverse, composed of innumerable libraries, frameworks, and components. It is common for
PHP developers to choose several of these and combine them into a single project. It is important that PHP code adhere
(as close as possible) to a common code style to make it easy for developers to mix and match various libraries for
their projects.

The [Framework Interop Group][fig] has proposed and approved a series of style recommendations. Not all of them related 
to code-style, but those that do are [PSR-0][psr0], [PSR-1][psr1], [PSR-2][psr2] and [PSR-4][psr4]. These recommendations 
are merely a set of rules that some projects like Drupal, Zend, Symfony, CakePHP, phpBB, AWS SDK, FuelPHP, Lithium, 
etc are starting to adopt. You can use them for your own projects, or continue to use your own personal style.

Ideally you should write PHP code that adheres to a known standard. This could be any combination of PSR's, or one 
of the coding standards made by PEAR or Zend. This means other developers can easily read and work with your code, 
and applications that implement the components can have consistency even when working with lots of third-party code. 

* [Read about PSR-0][psr0]
* [Read about PSR-1][psr1]
* [Read about PSR-2][psr2]
* [Read about PSR-4][psr4]
* [Read about PEAR Coding Standards][pear-cs]
* [Read about Zend Coding Standards][zend-cs]
* [Read about Symfony Coding Standards][symfony-cs]

You can use [PHP_CodeSniffer][phpcs] to check code against any one of these recommendations, and plugins for text editors 
like [Sublime Text 2][st-cs] to be given real time feedback. 

Use Fabien Potencier's [PHP Coding Standards Fixer][phpcsfixer] to automatically modify your code syntax so that it
conforms to these standards, saving you from fixing each problem by hand.

English is preferred for all symbol names and code infrastructure. Comments may be written in any language easily readable 
by all current and future parties who may be working on the codebase.

[fig]: http://www.php-fig.org/
[psr0]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md
[psr1]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md
[psr2]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md
[psr4]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md
[pear-cs]: http://pear.php.net/manual/en/standards.php
[zend-cs]: http://framework.zend.com/wiki/display/ZFDEV2/Coding+Standards
[symfony-cs]: http://symfony.com/doc/current/contributing/code/standards.html
[phpcs]: http://pear.php.net/package/PHP_CodeSniffer/
[st-cs]: https://github.com/benmatselby/sublime-phpcs
[phpcsfixer]: http://cs.sensiolabs.org/
