# Contenu de la V1

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
