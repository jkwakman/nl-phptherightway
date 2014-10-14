---
isChild: true
anchor: composer_and_packagist
---

## Composer en Packagist {#composer_and_packagist_title}

Composer is een **briljant** pakketbeheersysteem PHP. Beschrijf je project afhankelijkheden in een `composer.json` bestand en met een paar eenvoudige commando's update composer automatisch je project afhankelijkheden.

Er zijn op dit moment al heel veel PHP libraries geschikt voor Composer en te gebruiken in je project. Deze "packages" staan vermeld op [Packagist][1], de officiële bron for PHP libraries die geschikt zijn voor Composer.

### Hoe kan ik Composer gebruiken?

Je kunt Composer lokaal installeren (in je huidige werkmap, al wordt dit niet langer aangeraden) of globaal (bv /usr/local/bin). In onderstaand voorbeeld gaan wij ervan uit dat je Composer lokaal wilt installeren. Voer het volgende commando uit vanuit de hoofdmap van je project:

    curl -s https://getcomposer.org/installer | php

Hiermee download je het bestand `composer.phar`. Je kunt dit bestand uitvoeren middels `php` om je project dependencies te beheren. <strong>Pas op:</strong> Indien je het bestand direct uitvoert naar de interpreter, controleer dan vooraf online of de code veilig is.

#### Installeren onder Windows

De meest eenvoudige manier voor Windows gebruikers om Composer te installeren is gebruik te maken van de [ComposerSetup][6] installer. Middels deze installer wordt Composer voor alle gebruikers geïnstalleerd en voegt composer toe aan je `$PATH` variabele zodat je `composer` vanuit iedere map kan aanroepen.

### Hoe kan ik Composer handmatig installeren?

De handmatige installatie van Composer is niet eenvoudig. Er kunnen echter verschillende redenen zijn waarom een developer liever deze methode verkiest i.p.v. de interactieve installatie routine. De interactieve installatie checked of je PHP installatie:

- versie recent genoeg is om te kunnen worden gebruikt
- `.phar` bestanden correct kunnen worden uitgevoerd
- bepaalde map rechten correct zijn
- bepaalde problematische extensies niet zijn geladen
- bepaalde `php.ini` instellingen zijn ingesteld

Bij handmatige installatie worden bovenstaande checks niet uitgevoerd. Onderstaand de methode voor het handmatig installeren van Composer:

    curl -s https://getcomposer.org/composer.phar -o $HOME/local/bin/composer
    chmod +x $HOME/local/bin/composer

Het pad `$HOME/local/bin` (of een andere map naar keuze) dient te worden toegevoegd aan je `$PATH` environment variabele. Op die manier kun je het `composer` commando uitvoeren.

Indien je in de documentatie leest dat je Composer dient uit te voeren middels het `php composer.phar install` commando kun je dit vervangen door:

    composer install
    
Deze sectie gaat er vanuit dat composer globaal is geïnstalleerd.

### Hoe definieer en installeer je dependencies

Composer houdt je project zijn afhankelijkheden bij in het bestand `composer.json`. Je kunt dit bestand handmatig aanpassen of Composer het voor je laten doen. Het `composer require` commando voegt een project dependency toe. Indien je nog geen `composer.json` hebt wordt deze aangemaakt. Hier is een voorbeeld waarmee [Twig][2] als dependency wordt toegevoegd aan je project.

	composer require twig/twig:~1.8

Als alternatief kun je het `composer init` commando gebruiken om een volledig `composer.json` bestand voor je project aan te maken. Zodra er een `composer.json` bestand is aangemaakt kun je met Composer alle dependencies naar de `vendors/` map downloaden en vervolgens installeren. Dit geldt ook voor andere projecten die je hebt gedownload en al voorzien zijn van een `composer.json` bestand:

    composer install

Voeg vervolgens onderstaand commandoregel toe aan je primaire PHP bestand zodat PHP weet dat je Composer zijn autoloader wil gebruiken voor het beheren van je dependencies.

{% highlight php %}
<?php
require 'vendor/autoload.php';
{% endhighlight %}

Nu kun je je project dependencies gebruiken en deze worden automatisch on demand geladen.

### Je dependencies updaten

Composer maakt het bestand `composer.lock` aan waarin wordt beschreven welke pakketten / versies zijn gedownload zodra `php composer.phar install` voor het eerst wordt uitgevoerd. Indien je je project met andere developers deelt and het bestand `composer.lock maakt deel uit van je project krijgt iedereen automatisch dezelfde versie indien men het commando `php composer.phar install` uitvoert. Om je dependencies te updaten dien je `php composer.phar update` uit te voeren.

Dit is handig indien je je versiebeheer flexibel wilt inrichten. Hierbij betekend bijvoorbeeld  ~1.8 dat de "versie minimaal 1.8.0 moet zijn, maar minder dan 2.0.x-dev". Je kunt ook een `*` als wildcard gebruiken zoals b.v. `1.8.*`. Het commando `php composer.phar update` update nu alle dependencies volgens de regels die je hebt opgesteld.

### Update notificaties

Om updates to ontvangen omtrent nieuwe versie releases kun je je inschrijven voor [VersionEye][3]. Dit is een webservice die GitHub en BitBucket accounts monitort en notificaties stuurt zodra er een nieuwe package release is.

### Dependencies controleren op kwetsbaarheden

De [Security Advisories Checker][4] is een webservice en command-line tool die je `composer.lock` bestand analyseert en je waarschuwt indien je je dependencies moet updaten.

* [Leer meer over Composer][5]

[1]: http://packagist.org/
[2]: http://twig.sensiolabs.org
[3]: https://www.versioneye.com/
[4]: https://security.sensiolabs.org/
[5]: http://getcomposer.org/doc/00-intro.md
[6]: https://getcomposer.org/Composer-Setup.exe

