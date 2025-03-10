Réponses aux questions :

	1	Quel est le service rendu par l'application ? 
	L'application "quelpoke" génère une page web qui affiche un Pokémon basé sur un nom fourni en paramètre. 
 	Elle utilise un algorithme de hachage SHA-1 pour déterminer un identifiant unique de Pokémon (entre 1 et 151), 
  	puis récupère le nom du Pokémon correspondant via l'API PokeAPI.

	2	Quel est le fonctionnement global ?
	◦	L'application écoute les requêtes HTTP sur une adresse et un port définis par les variables d'environnement (ADDR et PORT).
	◦	Lorsqu'un utilisateur accède à la page via une requête GET avec un paramètre name, 
 		elle calcule un identifiant de Pokémon à partir de ce nom.
	◦	Elle interroge l'API externe PokeAPI pour récupérer le nom du Pokémon correspondant.
	◦	Enfin, elle affiche une page HTML en utilisant un modèle (index.tmpl.html) et les données obtenues.

	3	Comment lancer le service sur son poste ?
	◦	Installer Go 
	◦	S'assurer d'avoir le fichier index.tmpl.html dans le même répertoire que le code.
	◦	Définir les variables d'environnement si nécessaire (ADDR et PORT).
	◦	Lancer le serveur avec la commande : go run main.go
	◦	
	◦	Accéder à l'application via un navigateur à l'adresse http://localhost:8080?name=Prénom
