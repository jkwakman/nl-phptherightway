---
isChild: true
anchor: mac_setup
---

## PHP op je Mac  {#mac_setup_title}

OS X heeft standaard PHP geïnstalleerd staan maar meestal betreft dit een verouderde versie. Mountain Lion
heeft 5.3.10, Mavericks heeft 5.4.17 en Yosemite heeft 5.5.9. Inmiddels is PHP 5.6 echter de laatste stabiele
versie die je wilt hebben draaien.

Er zijn meerdere methoden om PHP te installeren op OS X.

### Installeer PHP via Homebrew

[Homebrew](http://brew.sh/) is een krachtige 'package manager' voor OS X die eenvoudig PHP en de diverse
extensies kan installeren. [Homebrew PHP] is een repository die alle benodigde PHP gerelateerde functionaliteit
bevat voor Homebrew en je eenvoudig PHP laat installeren.

Op dit moment kun je `php53`, `php54`, `php55` of `php56` installeren middels het `brew install` commando en wisselen tussen de verschillende versies middels de `PATH` variabele.

### Installeer PHP via phpbrew

Middels [phpbrew] kun je verschillende PHP versies installeren en beheren. Dit kan erg handig zijn indien je project verschillende versies van PHP vereist en je geen virtuele omgevingen wilt gebruiken.

### Compileer de broncode

Een andere optie die je kunt overwegen is het [zelf compileren][mac-compile] van de PHP broncode.
In dat geval dien je wel Xcode te installeren of Apple's variant ["Command Line Tools for XCode"] te downloaden uit de Apple Mac Dev Center.

### Alles-in-1 installatie

Bovenstaande oplossingen bieden alleen uitkomst voor PHP maar zorgen niet voor zaken zoals Apache, Nginx of SQL server. Alles-in-1 oplossingen zoals [MAMP][mamp-downloads] en [XAMPP][xampp] installeren wel deze andere
software en zorgen voor een werkend geheel. Alles-in-1 installaties zijn dus eenvoudig op te zetten maar zijn in de regel hierdoor wel minder flexibel.

[Homebrew]: http://brew.sh/
[Homebrew PHP]: https://github.com/Homebrew/homebrew-php#installation
[mac-compile]: http://www.php.net/manual/en/install.macosx.compile.php
[xcode-gcc-substitution]: https://github.com/kennethreitz/osx-gcc-installer

["Command Line Tools for XCode"]: https://developer.apple.com/downloads
[mamp-downloads]: http://www.mamp.info/en/downloads/
[phpbrew]: https://github.com/phpbrew/phpbrew
[xampp]: http://www.apachefriends.org/en/xampp.html
