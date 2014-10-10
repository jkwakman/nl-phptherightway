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

PHP stelt twee speciale variabelen beschikbaar binnen de argumenten van je script. [`$argc`][argc] is een integer variabele die het aantal argumenten *telt* en [`$argv`][argv] is een array variabele die de *waarde* van ieder argument bevat. Het eerste argument is altijd de naam van je PHP bestand, in dit geval dus `hello.php`.

Het `exit()` commando wordt gebruikt met een getal groter dan nul om de shell te laten weten dat het commando niet succesvol was. Veel gebruikte exit codes kunnen [here][exit-codes] worden bekeken.

Om bovenstaand script uit te voeren dien je het volgende in de command-line te typen:

{% highlight bash %}
> php hello.php
Usage: php hello.php [name]
> php hello.php world
Hello, world
{% endhighlight %}


 * [Leer meer over PHP uitvoeren op de command-line][php-cli]
 * [Leer meer over het gebruik van PHP op de command-line onder Windows][php-cli-windows]

[phpinfo]: http://php.net/manual/en/function.phpinfo.php
[cli-options]: http://www.php.net/manual/en/features.commandline.options.php
[argc]: http://php.net/manual/en/reserved.variables.argc.php
[argv]: http://php.net/manual/en/reserved.variables.argv.php
[php-cli]: http://php.net/manual/en/features.commandline.php
[php-cli-windows]: http://www.php.net/manual/en/install.windows.commandline.php
[exit-codes]: http://www.gsp.com/cgi-bin/man.cgi?section=3&topic=sysexits
