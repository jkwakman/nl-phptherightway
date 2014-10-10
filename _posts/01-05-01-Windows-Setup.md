---
isChild: true
anchor: windows_setup
---

## PHP onder Windows {#windows_setup_title}

PHP onder Windows kan op verschillende manieren worden geïnstalleerd. Je kunt [de binaire bestanden downloaden][php-downloads] en tot
voor kort kon je een '.msi' bestand installeren. Deze methode wordt echter niet meer ondersteund vanaf PHP versie 5.3.0.

Voor educatieve doeleinden en development op je eigen PC kun je de ingebouwde webserver gebruiken (beschikbaar vanaf PHP 5.4+) en hoef je je geen zorgen te maken
over configuratie. Indien je een alles-in-1 oplossing wenst met MySQL kun je software gebruiken zoals [Web Platform Installer][wpi], [Zend Server CE][zsce],
[XAMPP][xampp], [EasyPHP][easyphp] en [WAMP][wamp]. Middels dit soort software kun je onder Windows snel aan de slag met het ontwikkelen van software.
Houd hierbij echter wel rekening dat het werken onder Windows subtiel afwijkt van de productie omgeving indien je de software oplevert onder Linux.

Draai je een productieomgeving onder Windows? Kies dan voor IIS7 aangezien deze versie het meest stabiel is en de beste performance geeft. Je kunt gebruik
maken van [phpmanager][phpmanager] (een grafische interface voor IIS7) om eenvoudig PHP te beheren en te configureren. IIS7 heeft FastCGI ingebouwd
en kan worden ingezet door PHP als een 'handler' te configuren. Voor meer informatie en support verwijzen wij naar de [pagina omtrent PHP van iis.net][php-iis].

[php-downloads]: http://windows.php.net
[phpmanager]: http://phpmanager.codeplex.com/
[wpi]: http://www.microsoft.com/web/downloads/platform.aspx
[zsce]: http://www.zend.com/en/products/server-ce/
[xampp]: http://www.apachefriends.org/en/xampp.html
[easyphp]: http://www.easyphp.org/
[wamp]: http://www.wampserver.com/en/
[php-iis]: http://php.iis.net/
