# Introduction à Rails

##Table des matières :
- La différence entre un site statique et un site dynamique
- Le MVC
- Les routes
- Les Bases de Données
- GET / POST
- Le concept de migration
- Les relations entre les models des BDD
- Les fonctions du CRUD


1.**La différence entre un site statique et un site dynamique**

Une page web statique est une page web dont le contenu ne varie pas en fonction des caractéristiques de la demande, c'est-à-dire qu'à un moment donné tous les internautes qui demandent la page reçoivent le même contenu.

Pour une page web dynamique, le contenu peut donc varier en fonction d'informations (heure, nom de l'utilisateur, formulaire rempli par l'utilisateur, etc.) qui ne sont connues qu'au moment de sa consultation.

2.**Le MVC**

Acronyme de *Model* - *View* - *Controller*, correspond à une artchitecture logicielle pour la création des applications web.

Un modèle (Model) contient les données à afficher.
ex : les algo, la configuration de l'application, la logique etc...c'est le coeur de l'application

Une vue (View) contient la présentation de l'interface graphique.
ex : page web, interface graphique du jeu etc....

Un contrôleur (Controller) contient la logique concernant les actions effectuées par l'utilisateur.
Il contrôle les données, transmet les informations entre la Vue et le Modèle (en cas d'action user...)

![Image of MVC](https://www.supinfo.com/articles/resources/175268/777/1.png)


3.**Les routes**

Les routes permettent d’interpréter les URL et d’orienter vers les bonnes actions des controlleurs. 
La configuration se trouve dans le fichier config/routes.rb . ex : 

```
get "users", to: "users#index"
post "users", to: "users#create"
```

Dans les contrôleurs, il existe sept routes très fréquemment utilisées : index, create, show, update, destroy, new, edit.



4.**Les bases de données**

Les BDD permettent de stocker des informations d'une facon structuré permettant de rapidemment s'en servir pour 
l'enrichir, la mettre à jour, l'analyser etc....le tout informatiquement :D
ex : nom d'utilisateur, mot de passe, commandes, sexe, ville etc...


5.**GET / POST**

GET et POST sont des méthodes d'accès définies dans le protocole HTTP et reprises dans la spécification HTML.
Le choix de la méthode dépend de la façon dont les données sont reçues, de la taille et la nature des données. 


--> GET
C'est la méthode la plus courante pour demander une ressource. Une requête GET est sans effet sur la ressource, il doit être possible de répéter la requête sans effet.

--> POST
Cette méthode doit être utilisée lorsqu'une requête modifie la ressource.



6.**Le concept de migration**

Cela définit comment évolue la base de donnée et les modifications à lancer pour faire évoluer la BDD.
Contrairement à une basé de données externalisé, les concepts sont disponible facilement et peuvent être manipulés
par une tout autre personne sur un projet.



7.**Les relations entre les models des BDD**





8.**Les fonctions du CRUD**

Un CRUD est un système de manipulation des données de la base : ça signifie Create, Read, Update, Delete

Autrement dit, on va faire une interface pour gérer nos données. Cela peut entre autres servir à créer une interface d'administration pour votre site.

Voici le lien entre ces differentes opérations et leur methodes en SQL et HTTP :

| Operations    | SQL           | HTTP  |
| ------------- |:-------------:| -----:|
| Create        | INSERT        | POST  |
| Read          | SELECT        | GET   |
| Update        | UPDATE        | PUT   |
| Delete        | DELETE        | DELETE|


Voici un exemple de ces fonctions sur une application de carnet d'adresse :

- Créer des contacts
- Lire un contact (liste, zone de recherche…)
- Mettre à jour un contact
- Supprimer un contact


