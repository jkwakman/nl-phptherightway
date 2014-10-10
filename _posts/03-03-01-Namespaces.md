---
isChild: true
anchor: namespaces
---

## Namespaces {#namespaces_title}

Zoals eerder al werd aangegeven kent de PHP gemeenschap een groot aantal developers die samen heel veel code schrijven.
Dit betekend dat één PHP library dezelfde klasse benaming kan gebruiken als een andere library. Wanneer beide libraries
in dezelfde namespace worden gebruikt zorgt dit voor conflicten.

_Namespaces_ lossen dit probleem op. Zoals beschreven in de PHP handleiding kunnen namespaces worden vergeleken met
de mappenstructuur van een besturingssysteem; twee bestanden met dezelfde naam kunnen naast elkaar bestaan in verschillende
mappen. Op dezelfde manier kunnen PHP klassen dus bestaan in verschillende PHP namespaces onder dezelfde naam.

Het is daarom belangrijk om je code in een namespace te plaatsen zodat andere developers het kunnen gebruiken zonder
conflicten te veroorzaken met andere libraries.

Het wordt dan ook aangeraden om namespaces te gebruiken (zoals beschreven in [PSR-0][psr0]) volgens een standaard
bestand, klasse en namespace conventie om plug en play code mogelijk te maken.

In december 2013 heeft PHP-FIG een nieuwe autoloading standaard in het leven geroepen namelijk [PSR-4][psr4]. Deze standaard
zal in de toekomst waarschijnlijk PSR-0 vervangen. Op dit moment kun je echter beide standaarden gebruiken. PSR-4 vereist
namelijk PHP 5.3 waardoor PHP 5.2 projecten genoodzaakt zijn om de PSR-0 standaard te gebruiken. Indien je echter voor je nieuwe
 applicatie van plan bent om een autoloader standaard te gebruiken is het zeker de moeite waard om PSR-4 te checken.


* [Lees meer over namespaces][namespaces]
* [Lees meer over PSR-0][psr0]
* [Lees meer over PSR-4][psr4]

[namespaces]: http://php.net/manual/en/language.namespaces.php
[psr0]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md
[psr4]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md