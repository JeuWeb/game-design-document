# Mécanismes du jeu

Ce document présente plus en détails les mécanismes du jeu.


## Parties

Le jeu est organisé en parties indépendantes les unes des autres. Une partie commence quand un administrateur la démarre et s'achève quand tous les personnages-joueurs sont morts.


Dans les itérations suivantes, plusieurs parties pourront avoir lieu en parallèle et un joueur pourra avoir un personnage dans plusieurs parties. Les parties pourront avoir des réglages différents : taille et contenu du plateau de jeu, rythme de rechargement des points d'action.



## Plateau de jeu

Le plateau de jeu est un quadrillage. Chaque case est un carré et dispose d'une illustation d'ambiance. L'ensemble du plateau représente une ville, vue du dessus.

Chaque case du plateau est un carré dont chaque côté peut être franchissable ou non : cela permet de représenter les murs des différents bâtiments et ainsi correspondre au visuel d'ambiance.

Les personnages, les zombies et les objets laissés au sol y sont représentés par des pions, dessinés sur les cases à la manière des points d'un dé à 6 faces. Cette disposition est purement visuelle et n'a aucun impact sur le jeu.

Les case peuvent être fouillées par les survivants dans l'espoir d'y trouver des objets utiles. Une pièce ne peut pas être fouillée indéfiniment.


Dans les itérations suivantes, le plateau s'ouvrira à l'espace périurbain qui borde la ville. Les portes entre les cases pourront être ouvertes, fermées, verrouillées, défoncées ou baricadées.



## Personnages

Les personnages sont les entités contrôlés par les joueurs. Quand il rejoint une partie, le joueur choisis le nom de son personnage avant d'être placé sur une case sûre du plateau de jeu, où son aventure commence.

Chaque personnage peut effectuer diverses tâches au prix d'un certain nombre de points d'action :

- Crier : les autres personnages (et zombies !) peuvent recevoir le message, même à 3 cases de distance.
- Parler : seuls les personnages (et zombies !) de la case et des cases adjacentes reçoivent le message.
- Chuchoter : seul le personnage choisi reçoit le message.
- Donner un objet : un personnage choisi sur la même case reçoit alors l'objet désigné.
- Déposer un objet : l'objet est alors placé sur la case, à la disposition de tous.
- Ramasser un objet : l'objet choisi sur la case est est alors placé dans l'inventaire du personnage.
- Se déplacer sur une case adjacente (haut, droite, bas, gauche).
- Attaquer : si la cible est sur la même case, on peut la choisir, si elle est sur une case plus éloignée (selon la portée de l'arme), la cible est déterminée aléatoirement (parmi les survivants et les zombies !).


Dans les itérations suivantes, la personnalisation des personnages sera mise en avant.



## Zombies

Les zombies sont joués par le système, ils agissent automatiquement à intervalles réguliers.

Quand vient leur tour, les zombies qui partagent la case d'au moins un personnage passent à l'attaque : ils frappent alors l'un des personnages présents, désigné aléatoirement, qui perd alors quelques points de vie.

Quand ils ne partagent pas la case d'un personnage et qu'un bruit retentit sur une case, les zombies à portée de ce bruit sont attirés : quand vient leur tour de jeu (propre à chacun), ils se déplacent en direction de ce bruit. Si un autre bruit les attire entre temps, ils se dirigent vers ce dernier.

Si un zombie n'a ni attaqué, ni suivi un bruit, il se déplace dans une direction aléatoire.


Au cours de la partie, de nouveaux zombies apparaissent parfois sur les cases en bordure du plateau de jeu.


### Les armes

Lorsqu'un personnage attaque un zombie ou un autre personnage, il le fait avec une arme. Chaque arme dispose d'une portée (0 pour une arme de corps à corps) et de plusieurs plages de dégâts (de l'échec du coup au coup critique) qui reflètent sa dangerosité.

Le résultat d'une attaque est déterminé aléatoirement : il indique la plage de dégâts utilisée pour cette attaque et la gravité de la blessure infligée.

Exemple :
Lors d'une attaque, un jet de dé entre 1 et 100 est effectué :

- Le katana rate entre 1 et 10, blesse légèrement (20 à 25 pv) entre 10 et 20 et blesse gravement (50 à 60 pv) entre 20 et 100.
- La casserole rate entre 1 et 20, blesse légèrement (10 à 15 pv) entre 20 et 70 et blesse gravement (15 à 20 pv) entre 70 et 100.


Dans les itérations suivantes, les caractéristiques du personnage lui permettront de progresser dans la maîtrise des armes, et ainsi d'améliorer son efficacité.
