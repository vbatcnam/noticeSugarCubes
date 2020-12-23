# SC.actionOn

```javascript 
SC.actionOn(evt, actionDeclancheSiEvtPresent, actionDeclancheSiEvtAbsant, nbreDinstant) 
```

SC.actionOn() est une construction qui a intuitivement la sémantique suivante :
* On regarde si une configuration événementielle est vérifiée (la configuration est le premier paramètre).
* Si la configuration est vraie à l’instant où cette instruction est exécutée on appelle la méthode passée en deuxième paramètre. 
* Si la configuration est fausse alors on exécute le troisième paramètre. 
* Le quatrième paramètre permet quant à lui de répéter l’opération en boucle sur un nombre d’intrants donné (par défaut 1 seul instant). 

*actionDeclancheSiEvtPresent* doit avoir 1 parametre. Ce parmetre sera rempli automatiquement avec un objet JS.
Cet objet JS aura 1 propriété par type d'évenement généré jusqu'au moment où la machine active l'actionON. 
Cette propriété a comme clé l'evenement et comme valeur un array qui contient la liste des valeurs générées avec cet évenement.
