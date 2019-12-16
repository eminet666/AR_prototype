# AR prototype

1 _ DE BLENDER A LA RÉALITÉ AUGMENTÉE (AR)
Cette maquette met en oeuvre des modalités d'animation et d'interaction en Réalité Augmentée dans la perspective de notre projet.

Etape 1 : BLENDER : modélisation->animation->export
L'article suivant décrit étape par étape toute cette procédure jusqu'à l'export
https://unboring.net/workflows/animation.html

Etape 2 : BLENDER export
Un article complet sur les objets 3D utilisables en AR sur le web :
https://medium.com/@akashkuttappa/using-3d-models-with-ar-js-and-a-frame-84d462efe498

Plusieurs formats d'export permettent d'enregistrer également les informations relatives aux informations :
- json (javascript object notation) -> celui utilisé dans cet exemple
- gltf2 (GL Transmission Format File)

Etape 3 : Intégration au code HTML/CSS/javascript pour une utilisation web
Ces fichiers sont directement utilisable dans la programmation web et c'est bien l'objet de cette maquette.
Pour plus de facilité, comme le code reste court, j'ai laissé le code javascript dans le fichier HTML.
Le fichier index.html est largement documenté pour vous en faciliter la compréhension.

2 _ FONCTIONNALITÉS
- La prototype intègre un export json (models/eva-animated.json) qui contient 4 animations incluses (idle/walk/run/hello)
- à partir de la reconnaissance d'un marker (hiro), l'animation se lance
- il y a plusieurs possibilités d'interactivité
  * 4 boutons HTML permettent de passer d'une animation à l'autre
  * il est aussi possible de cliquer directement sur le personnage pour le faire courrir ... à condition que le curseur 3D (rond rouge) soit sur le personnage au moment du clic

3 _ UTILISATION
Pour tester, vous savez faire (http-server et ngrok sont déjà installés):
- lancer un terminal à partir du répertoire qui contient le fichier index.html et index_min.html (sans interactivité, 1 seule animation)
et lancer la commande 'http-server' (lance le serveur sur le port 8080 par défaut)
- ensuite dans une autre fenêtre terminal, lancer la commande 'ngrok http 8080'
- copier dans le presse-papier l'adresse https://xxxxxxxx/ngrok.io
- et la copier dans la basse d'adresse d'un navigateur

J'ai testé avec Chrome sur mac, et Safari sur iphone (iOS).
Vous me direz si vous rencontrez des difficultés sur d'autres navigateurs et autres smartphones.

4 _ EXPÉRIMENTATION
- En suivant la procédure d'export présentée dans l'article https://unboring.net/workflows/animation.html, vous exporterez votre animation dans un format json.
- vous placerez votre fichier json exporté et vous le placerez dans le répertoire models de l'arborescence
- vous mettez à jour le nom du fichier json dans le fichier index_min.html
Commencer avec le fichier index_min.html qui n'intègre pas d'interactivité et n'utilise qu'une seule des animations.
Si vous arrivez à intégrer votre modèle exporter en json, vous pouvez essayer avec plusieurs animations dans le même fichier et l'interactivité.

- et vous testez !
NB : pour vérifier que vous n'avez pas fait d'erreur dans le code, utilisez la console des outils de développement de chrome (alt+cmd+i).
(Il est normal que le fichier favicon.ico soit manquant)

Good luck !
