# SC.action()

```javascript 
SC.actionOn(evt, actionDeclancheSiEvtPresent, actionDeclancheSiEvtAbsant, nbreDinstant);
``` 

SC.action() : est une action atomique au sens des SugarCubes. Cela veut dire qu’elle s’exécute intégralement de manière atomique au cours de l’instant ou l’instruction SC.action est activée par le moteur réactif. 

SC.action() fait une action externe qui ne fait pas partie de SC

L’action est une fonction javascript. Dans le cadre d’un cube (sorte d’objet réactif). L’action est une méthode de l’objet javascript associé.

SC.actionOn() est une construction qui a intuitivement la sémantique suivante :

- On regarde si une configuration événementielle est vérifiée (la configuration est le premier paramètre).
- Si la configuration est vraie à l’instant où cette instruction est exécutée on appelle la méthode passée en deuxième paramètre. 
- Si la configuration est fausse alors on exécute le troisième paramètre. 
- Le quatrième paramètre permet quant à lui de répéter l’opération en boucle sur un nombre d’intrants donné (par défaut 1 seul instant). 
		
##SC.action(SC.my("fonction")) 

Ceci représente une action atomique qui à l’instant où elle est exécutée va provoquer l’exécution de la méthode java script de l’objet javascript associé au cube. C’est tout…

En fait pas tout à fait, ;-). Il y a un deuxième paramètre avec SC.action :