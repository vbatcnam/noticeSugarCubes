# SC.my()

L’instruction SC.my() Permet de récupérer le champ d’un objet associé par un cube. 
Par exemple : 
```javascript
SC.my("sc_requestDisplayFun");
```
permet de récupérer la méthode ```sc_requestDisplayFun()``` du canvas.
	
L’instruction ```SC.my()``` réalise l’association à runtime (car à l’écriture du programme on ne connaît pas encore le cube dans lequel cette instruction va être exécutée et donc on ne connaît pas non plus l’objet javascript sur lequel il va falloir appeler la méthode ).
