# Readme

## Wat is dit?

De eerstejaarsstudenten toegepaste informatica aan de KHLeuven leren programmeren in assembly. Om dingen die doorgaans ietwat ingewikkeld zijn (zoals I/O) te vereenvoudigen wordt er ons een soort mini-framework aangeboden, bestaande uit:

- `gtine.obj`: een object-file met een aantal subroutines
- `gt.asm`: bestandje met een aantal nasm-macro's om het gebruik van de voorgedefiniëerde macro's te vereenvoudigen
- `vertaal.bat`: een DOS-script om het omzetten door nasm te vereenvoudigen
- `voeruit.bat`: een DOS-script om het linken en uitvoeren van de uiteindelijke executable te vereenvoudigen

## Jaja, maar wat is dit dan?

Elk van die bestanden is windows-specifiek. Studenten die geen Windows gebruiken, kunnen de oefeningen dus niet op hun eigen laptop maken. Dit project biedt een oplossing.

Al de subroutines voor het lezen en schrijven van en naar bestanden en de commandline zijn (blind) herschreven. Dat wil zeggen, zonder naar de assembly te kijken. Bij dit project krijg je de code van al die subroutines er ook bij, kwestie van educatief te zijn enzo.

- `gtine.asm`: een bestandje met subroutines en macro's. Voor dat het kan worden gebruikt (achter de schermen) bij het linken van de executable, moet dit eerst in een object-file worden omgezet. Dat kan met `./vertaal gtine`.
- `gt.asm`: zelfde functie als bij de windows-versie
- `vertaal`: bash-script met zelfde functie als `vertaal.bat`
- `voeruit`: bash-script met zelfde functie als `voeruit.bat`
- `unistd.txt`: documentatie met enkele POSIX constanten

## En hoe gebruik ik dit, dan?

### Benodigdheden

Eerst heb je een aantal dingen nodig:

- de assembler, *nasm*
- de linker, *ld*

Voor installatie-instructies, raadpleeg je package-manager.

### Verder ook nog

Je hebt natuurlijk ook enkele bestanden nodig die je hier kan vinden:

- gtine.asm
- gt.asm
- vertaal
- voeruit

De bash-scripts geef je best executable permissies: `chmod +x vertaal voeruit`

Je moet ook gtine.asm omzetten in een object-file. Dit kan als volgt: `./vertaal gaine`

### En dan?

Vanaf dat moment kan je deze bestanden op een vergelijkbare manier gebruiken als op Windows. Vertalen met `./vertaal` in plaats van `vertaal`, uitvoeren met `./voeruit` in plaats van `vooruit`.

Meer is er niet aan.
