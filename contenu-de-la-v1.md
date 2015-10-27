# Contenu de la V1-Update
- Le jeu se présentera sous forme de partie
  - Une partie peut :
    - Contenir X joueurs
    - Avoir des paramétrages différents (difficulte, nombre de joueurs, de zombies etc..)
    - S'arrêtent quand il n'y a plus de joueurs vivants (si personne ne peut rejoindre la partie une fois commencée)

- Création d'un personnage dans une partie : on lui donne simplement un nom.
  - Les personnages ont 3 jauges :
    - La santé.
    - La faim : quand la jauge de faim se vide, la santé diminue.
    - La soif : quand la jauge de soif se vide, la santé diminue (rapidement).
  - Chaque joueur possède 24h d'actions par jour. Ex : se déplacer d'une case prends 20 minutes (mais est instantané)
  - Il dispose d'un équipement et d'un inventaire, avec une limite globale de poids.
  - Un personnage peut faire plusieurs actions :    
    - Fouiller une pièce ou une case (il peut alors utiliser directement l'objet, le stocker dans son inventaire ou le laisser au sol).
    - Utiliser des objets (nourriture, pour remonter sa jauge).
    - Attaquer un zombie ou un joueur (avec une arme de corps à corps ou une arme à feu)
      - Quand il tire dans le tas, il ne choisit pas qui est touché (joueur ou zombie)
    - Crier (entendus de loin), à voix basse (entendu localement), chuchoter (entendu par le destinataire proche uniquement).
    - Echanger des objets avec un autre joueur.
    - Se déplacer.
    - Se mettre en mode furtif (à réfléchir)
      - Se déplacer en mode furtif sur une autre case permet d'arriver et de ne pas être détecté par les zombies (calcul jet)
      - Attaquer en mode furtif... 
    - Chaque action génère du bruit, lié à la case
      - Les zombies étant attirés par le bruit, ils se dirigeront vers la case en générant le plus.
      - Ex : Je tire au flingue sur le case A1, je génère 3 de bruits, les zombies à 3 cases aux alentours se dirigent vers la case A1 (voir plus bas : Les zombies)

- Les zombies
  - Un certain nombre de zombie sera créé lors de la création de la partie, le reste arrivera au fur et à mesure, aléatoirement des bords de la carte, et se déplacera aléatoirement ou via les actions des joueurs.
    - Chaque zombie sera géré à part entière et aura un timer aléatoire (x minutes). Il est inactif jusqu'à la fin du timer, à la fin de ce timer, il fait son action, reinitialise le timer et re-attend la fin. Un zombie peut faire 3 actions :
      - Attaquer
        - Un zombie essayera toujours d'attaquer les joueurs sur sa case. Dans le cas où il n'y a rien à attaquer, il se déplace ou ne fait rien.
      - Se déplacer
        - Vers une case aléatoire si aucun évènement particulier n'est signalé
        - Vers une case ayant généré du bruit. La case ayant généré le plus de bruit prenant toujours le dessus. Ex : Je génère 3 de bruits sur la case A1, les zombies jusqu'à trois cases seront attirés vers A1. Si entre temps, un autre joueur génère 4 bruits non loin de ces mêmes zombies, ils changeront de direction pour aller vers la case à 4 bruits.
        - Vers un joueur qui est détecté et qui a changé de case
        - Vers un autre zombie ayant changé de case (effet boule de neige, création de hordes)
        - Le zombie arrête immédiatement de se déplacer s'il croise un joueur (on passe donc à l'attaque)
      - Ne rien faire

- Plateau de jeu
  - Affichage du plateau de jeu en vue de dessus, case par case.
  - Spawn de départ dans une ville, dans une safe zone bien gardée. Une fois dehors la survie commence.
  - Petite carte pour commencer, une ville et quelques zones plus tranquilles.

- Génération des objets "à fouiller" dans chaque pièce (nourriture, protections ou armes).

- L'inventaire

- Les items


  # Contenu de la V1-Old

- Création d'un personnage dans une partie : on lui donne simplement un nom.
  - Les personnages ont 2 jauges :
    - La santé.
    - La faim : quand la jauge de faim se vide, la santé diminue (rapidement).
  - Les points d'action sont rechargés régulièrement.
  - Il dispose d'un équipement et d'un inventaire, avec une limite globale de poids.
  - Un personnage peut fouiller une pièce (il peut alors utiliser directement l'objet, le stocker dans son inventaire ou le laisser au sol).
  - Un personnage peut utiliser des objets (nourriture, pour remonter sa jauge).
  - Il peut attaquer un zombie ou un joueur (avec une arme de corps à corps ou une arme à feu) : quand il tire dans un tas, il ne choisit pas qui est touché (joueur ou zombie).
  - Il peut crier (entendus de loin), à voix basse (entendu localement), chuchoter (entendu par le destinataire proche uniquement).
  - Il peut échanger des objets avec un autre joueur.
  - Il peut se déplacer.
  - Il peut se mettre en mode furtif (qui augmente le coût des actions mais diminue les chances d'être vu ou pris pour cible).

- Plateau de jeu
  - Affichage du plateau de jeu en vue de dessus.
  - Spawn des zombies de départ.
  - Spawn de zombies additionnels.
  - Déplacement des zombies dans la direction du bruit le plus important, ou aléatoirement sinon.
  - Les points d'actions des zombies sont également rechargés régulièrement (individuellement pour chacun).
  - Attaque des zombies sur les personnages (des moins discrets au plus discrets), quand il y en a à portée.
  - Génération des objets "à fouiller" dans chaque pièce (nourriture, protections ou armes).