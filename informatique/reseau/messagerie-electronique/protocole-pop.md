# 🕒 Protocole POP

## Présentation du POP :&#x20;

Le POP (Post Office Protocol) est un protocole de messagerie électronique utilisé pour récupérer les e-mails d'un serveur distant vers un client de messagerie. Contrairement au SMTP qui se concentre sur l'envoi des e-mails, le POP se concentre sur la réception des e-mails.

## Rôles et fonctionnement du POP :&#x20;

Le rôle principal du POP est de permettre au client de messagerie de se connecter au serveur POP et de récupérer les e-mails. Le client se connecte généralement au serveur POP à l'aide du port 110. Le serveur POP stocke les e-mails dans une boîte aux lettres jusqu'à ce que le client se connecte et les télécharge. Lorsque le client récupère les e-mails, ils sont généralement supprimés du serveur, bien que cela puisse être configuré différemment.

## Étapes de récupération des e-mails via le POP :

1. Établissement de la connexion : Le client de messagerie établit une connexion TCP avec le serveur POP à l'aide du port 110.
2. Authentification : Le client s'authentifie en fournissant les informations d'identification nécessaires, telles que le nom d'utilisateur et le mot de passe.
3. Téléchargement des e-mails : Une fois authentifié, le client demande au serveur POP de lui fournir la liste des e-mails disponibles. Ensuite, il télécharge les e-mails choisis sur le client de messagerie.
4. Marquage des e-mails : En fonction des paramètres de configuration, les e-mails peuvent être marqués comme lus ou supprimés sur le serveur POP.
5. Déconnexion : Le client se déconnecte du serveur POP.

## Limitations du POP :&#x20;

Le protocole POP présente certaines limitations. Tout d'abord, il ne prend généralement pas en charge la synchronisation des e-mails entre plusieurs appareils. De plus, puisque les e-mails sont généralement téléchargés et supprimés du serveur, il peut être difficile d'accéder aux e-mails depuis différents clients ou périphériques. Cela peut poser des problèmes si vous utilisez plusieurs appareils pour accéder à vos e-mails.

Le POP reste cependant un protocole largement utilisé pour récupérer les e-mails, en particulier dans les environnements où la conservation des e-mails sur le serveur n'est pas une exigence essentielle.
