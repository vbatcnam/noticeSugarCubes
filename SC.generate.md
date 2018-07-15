# SC.generate()

SC.generate(evt, valeurAssocieAEvt, nbreDinstant) est une instruction SugarCubes qui génère un événement à un instant précis. C’est à dire qu’elle « dit » que l’événement est présent à cet instant. Il s’agit là de la partie booléenne de l’information : un événement à chaque instant est soit présent (il a été émis) soit absent (personne ne l’a émis). On peut utiliser cette information booléenne dans plein de tests pour réagir à la présence ou l’absence d’un événement.
Mais un événement possède également une liste de valeurs associées à chaque émission ayant lieu au cours du même instant. C’est cette liste de valeurs qui sera traitée par les autres éléments en parallèle en particulier les instruction SC.actionOn…

SC.generate(evt, SC.my("fonction")), ici on dit à l’instant ou cette instruction est exécutée par le moteur réactif on émet l’événement. L’événement sera donc présent à l’instant exact ou il est émis. Et tout le monde pourra le voir et réagir à la présence de cet événement de façon totalement déterministe.
L'evenement ainsi généré va intéresser les autres objet. Mais ici on ne le fait qu’une fois au premier instant ce qui est ennuyeux puisqu’aux instants suivants cet événement n’est plus émis :
Donc si on veut émettre l’événement à chaque instant, il faudrait écrire :
```javascript 
SC.generate(evt, SC.my("fonction"), SC.forever);
```
