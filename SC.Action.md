# SC.action()

SC.action() fait une action externe qui ne fait pas partie de SC

SC.action() : est une action atomique au sens des SugarCubes. Cela veut dire qu’elle s’exécute intégralement de manière atomique au cours de l’instant ou l’instruction SC.action est activée par le moteur réactif. 

L’action est une fonction javascript. Dans le cadre d’un cube (sorte d’objet réactif). L’action est une méthode de l’objet javascript associé.