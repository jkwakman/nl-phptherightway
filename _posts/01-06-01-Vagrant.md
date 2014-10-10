---
isChild: true
anchor: vagrant
---

## Vagrant {#vagrant_title}

Indien je ontwikkelomgeving en productieomgeving van elkaar afwijken kunnen er rare bugs ontstaan op het moment dat je
applicatie live gaat. Het is daarnaast erg lastig om de verschillende ontwikkelomgevingen up-to-date te houden
(met dezelfde software versies) indien je werkt in een team van meerdere developers.

Indien je werkt onder Windows en je je software publiceerd onder Linux (of een ander niet-Windows OS) of werkt in een team
zou je moeten overwegen om een virtuele machine te gebruiken. Dit lijkt complex maar middels [Vagrant][vagrant] kun je
eenvoudig een virtuele machine opzetten. Deze 'base boxes' kun je handmatig aanmaken of je kunt gebruik maken van "inricht"
software zoals [Puppet][puppet] of [Chef][chef] om het voor je te doen. Het inrichten van een base box is een handige
manier om te garanderen dat meerdere machines op exact dezelfde manier zijn opgezet en dit zorgt voor minder onderhoud.
Je kunt een base box ook heel gemakkelijk verwijderen en opnieuw aanmaken waardoor het eenvoudig is om een nieuwe installatie
aan te maken.

Vagrant maakt mappen aan zodat je eenvoudig je code kunt delen tussen je PC en de virtuele machine. Op die manier kun je
bestanden op je lokale PC aanmaken en wijzigen en de code vervolgens laaten draaien op de virtuele machine.

### Hulp nodig?

Indien je support nodig hebt bij het gebruik van Vagrant raden wij onderstaande services aan:

- [Rove][rove]: Service die standaard Vagrant builds beschikbaar stelt die je kunt gebruiken (b.v. PHP). Dit alles wordt mogelijk
  gemaakt middels Chef.
- [Puphpet][puphpet]: simple grafische interface voor het opzetten van virtuele machines die geschikt zijn voor PHP development. **Deze service is sterk gericht op PHP**.
  Naaste lokale VM's kan men ook virtuele machines in de cloud aanmaken. Dit alles wordt mogelijk gemaakt middels Puppet.
- [Protobox][protobox]: is een softwarelaag bovenop vagrant zodat je middels een webinterface eenvoudig virtuele machines kan aanmaken die geschikt zijn voor webdevelopment.
  Middels een enkel YAML bestand kun je bepalen wat er op de virtuele machine moet worden geïnstalleerd.
- [Phansible][phansible]: eenvoudige interface voor het genereren van Ansible Playbooks voor PHP projecten.

[vagrant]: http://vagrantup.com/
[puppet]: http://www.puppetlabs.com/
[chef]: http://www.opscode.com/
[rove]: http://rove.io/
[puphpet]: https://puphpet.com/
[protobox]: http://getprotobox.com/
[phansible]: http://phansible.com/
