## le jeu icaRius et le moteur solarus

Solarus est un moteur de jeu Open Source, spécifiquement conçu pour créer des "role playing games" (RPG) en 2D, à l'image de *The Legend of Zelda: A Link to the Past* ou *Secret of Mana* sur Super Nintendo. Le site [solarus-games](https://www.solarus-games.org/) permet d'accèder à l'ensemble des ressources : le moteur de jeu, les packs de ressources (programmes, ensemble de graphismes appelés tilesets), les tutoriels...

Le moteur Solarus est codé en C++, avec la bibliothèque SDL et un backend OpenGL. Les jeux faits avec Solarus sont appelés des quêtes et son fait en Lua. Le moteur fait tous les calculs lourds (par exemple : tests de collisions) et les opérations bas-niveau comme dessiner à l'écran, animer les sprites et jouer du son. Pour "jouer" les quêtes, il suffit de télécharger le [runner Solarus](https://www.solarus-games.org/fr/solarus/download). Mais pour développer sa propre quête ou pour contribuer à l'édition d'une quête dans une optique communautaire, il vous faudra installer le [Solarus Quest Editor](https://www.solarus-games.org/fr/solarus/download)

Un créateur de quête n'a pas à implémenter ces algorithmes. Au contraire, il peut se concentrer sur la définition de la logique du jeu. Le créateur, par des scripts Lua, décrit le comportement des ennemis, les interactions sur une carte de jeu (une *map*). Il peut aussi créer des menus, des animations, un HUD (informations à l'écran comme le nombre de vies de la partie en cours, l'équipement du héros...).

Les deux parties (le moteur en C++ et les scripts en Lua) communiquent grâce à l'API Lua de Solarus. La communication fonctionne dans les deux sens : le créateur de quête peut appeler des fonctions du moteur (par exemple : déplacer un personnage) et le moteur appellera les propres fonctions du créateur de quête (par exemple : être informé quand un ennemi est tué). 

Mais avant d'utiliser l'API Lua de Solarus, il faut apprendre les bases du Lua (un langage simple et minimal, mais très puissant). Les [tutoriels vidéos](https://www.solarus-games.org/fr/development/tutorials/solarus-video-tutorial) sont un bon moyen pour débuter, expliquant étape par étape comment construire les éléments classiques : maps, menus, cinématiques, énigmes, donjons, ennemis, etc.  La [documentation de l'API Lua](https://www.solarus-games.org/doc/latest/) de Solarus est là où vous devez chercher dès que vous avez une question sur l'utilisation de cette API.

Vous avez vu les bases en lua ? Vous connaissez l'organisation d'ensemble d'une quête Solarus et les fonctions de l'éditeur de quête ? Vous pouvez désormais contribuer au développement du jeu icaRius, directement via [le dépôt gitlab](https://git.lab.sspcloud.fr/funcamp-r/funcamp-r-icarius) avec le code source de la quête correspondante.


