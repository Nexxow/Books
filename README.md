# TrelloBooks-server

Planificateur de lecture de livre. Prendre un livre et l’avoir sur son trello personnel dans différentes catégories.

Du coté services : On aura besoin de https://developers.google.com/books/docs/overview  et https://trello.readme.io/docs/api-introduction , la méthode principale serait de prendre un livre en entrée la colonne visée sous trello. On transforme l’objet livre en carte trello. Puis on l’ajoute à la colonne visée. Par exemple, à lire, à acheter, en cours de lecture … De plus, on a besoin d’un compte (contenant un token trello) en entrée pour chaque utilisateur.
Il y a donc aussi une présence d’un compte lié à ce token, donc il y aura une fonction de login et une fonction de création de compte. Celui-ci permettra d’avoir comme méthode de retrouver l’historique des ajouts de livres sous trello pour un utilisateur donné.

Coté client : Il y a une page de connexion et de création de compte (où l’utilisateur liera son compte à un compte trello). L’utilisateur recherche un livre. Pour rechercher un livre, il choisira la catégorie du livre ou s’il a un auteur préféré. S’il est intéressé par un livre, il pourra avoir plus d’informations sur le livre en cliquant  “en savoir plus”, ensuite le livre pourra être placé dans le trello (s’il l’a, s’il veut l’acheter, s’il est intéressé sans plus, s’il l’a déjà, ...). On aura ensuite un trello avec tous les livres triés par l'utilisateur et pourra toujours les faire passer d’une catégorie à une autre.

Persistence : Stockage des comptes et de son historique, sous mongoDB.
