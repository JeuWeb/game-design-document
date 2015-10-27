# Fonctionnalités de la V1

La première itération du projet se veut minimaliste tout en étant jouable : elle jette les fondations du jeu.

## Personnage

- Création d'un personnage dans une partie : on lui donne simplement un nom.
- Les personnages sont tous identiques (en dehors d'un nom). Ils ont une jauge de santé et des points d'action.
- Les points d'action sont rechargés régulièrement (à chaque joueur son heure de recharge).
- Il dispose d'un inventaire constitués de plusieurs emplacements : chaque objet ramassé occupe un emplacement.
- Un personnage peut fouiller une pièce, avec la probabilité de trouver une arme, qu'il peut alors ramasser ou laisser au sol.
- Il peut se déplacer.
- Il peut crier (bruyant), parler (peu bruyant) ou chuchoter (aucun bruit).
- Il peut échanger des objets avec un autre joueur.
- Il peut attaquer un zombie ou un joueur à portée de son arme.

## Plateau de jeu & zombies

- Affichage du plateau de jeu en vue de dessus.
- Répartition aléatoire des zombies de départ.
- Génération régulière de zombies supplémentaires sur les bords du plateau.
- Déplacement des zombies dans la direction du bruit le plus important, ou aléatoirement sinon.
- Les points d'actions des zombies sont également rechargés régulièrement (individuellement, à chaque zombie son heure de recharge).
- Attaque des zombies sur les personnages (des moins discrets au plus discrets), quand il y en a à portée.
