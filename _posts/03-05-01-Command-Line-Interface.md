---
isChild: true
anchor: command_line_interface
---

## Command-line-interface {#command_line_interface_title}

PHP is gemaakt om webapplicaties mee te schrijven maar is ook handig bij het schrijven van command-line-interface (CLI) programma's. CLI PHP programma's kunnen je helpen bij het automatiseren van taken zoals testen, deployment en applicatiebeheer.

CLI PHP programma's zijn erg krachtig omdat je de code van de applicatie direct kan aanroepen zonder de noodzaak om een beveiligde webinterface te schrijven. Plaats echter nooit je CLI scripts in je publieke web root!

Probleer zelf maar eens om PHP uit te voeren vanaf de command-line:

{% highlight bash %}
> php -i
{% endhighlight %}

De `-i` optie toont je de PHP configuratie net zoals de [`phpinfo`][phpinfo] functie.

De `-a` optie toont je een interactieve shell, soortgelijk als ruby's IRB of python's interactieve shell. Uiteraard zijn er nog meer andere handige [command-line opties][cli-options] beschikbaar.

Laten wij een simpel "Hello, $name" CLI programma schrijven. Om het programma uit te voeren dien je een bestand `hello.php` aan te maken zoals onderstaand.

{% highlight php %}
<?php
if ($argc != 2) {
    echo "Usage: php hello.php [name].\n";
    exit(1);
}
$name = $argv[1];
echo "Hello, $name\n";
{% endhighlight %}

PHP sets up two special variables based on the arguments your script is run with. [`$argc`][argc] is an integer variable containing the argument *count* and [`$argv`][argv] is an array variable containing each argument's *value*. The first argument is always the name of your PHP script file, in this case `hello.php`.

The `exit()` expression is used with a non-zero number to let the shell know that the command failed. Commonly used exit codes can be found [here][exit-codes]

To run our script, above, from the command line:

{% highlight bash %}
> php hello.php
Usage: php hello.php [name]
> php hello.php world
Hello, world
{% endhighlight %}


 * [Learn about running PHP from the command line][php-cli]
 * [Learn about setting up Windows to run PHP from the command line][php-cli-windows]

[phpinfo]: http://php.net/manual/en/function.phpinfo.php
[cli-options]: http://www.php.net/manual/en/features.commandline.options.php
[argc]: http://php.net/manual/en/reserved.variables.argc.php
[argv]: http://php.net/manual/en/reserved.variables.argv.php
[php-cli]: http://php.net/manual/en/features.commandline.php
[php-cli-windows]: http://www.php.net/manual/en/install.windows.commandline.php
[exit-codes]: http://www.gsp.com/cgi-bin/man.cgi?section=3&topic=sysexits
