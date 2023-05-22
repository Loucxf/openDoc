# 🕑 Protocole SMTP

## Présentation du SMTP :&#x20;

Le SMTP (Simple Mail Transfer Protocol) est le protocole standard utilisé pour l'envoi d'e-mails. Il définit les règles et les procédures de transmission des messages d'un client de messagerie vers un serveur de messagerie. Le SMTP est largement adopté et permet l'acheminement des e-mails à travers Internet.

## Fonctionnement du SMTP :&#x20;

Le fonctionnement du SMTP implique plusieurs étapes. Tout d'abord, le client de messagerie se connecte au serveur SMTP du destinataire à l'aide du port 25. Ensuite, le client envoie les informations sur l'expéditeur, le destinataire et le contenu du message au serveur SMTP. Le serveur SMTP du destinataire vérifie ensuite si le destinataire est valide et s'il peut accepter le message. Si tout est en ordre, le serveur SMTP enregistre le message dans la boîte aux lettres du destinataire.

## Étapes de transmission d'un e-mail via le SMTP

1. Établissement de la connexion : Le client de messagerie établit une connexion TCP avec le serveur SMTP du destinataire.
2. Envoi du message : Le client de messagerie envoie le message en utilisant des commandes SMTP telles que "MAIL FROM" (pour spécifier l'expéditeur), "RCPT TO" (pour spécifier le destinataire) et "DATA" (pour envoyer le contenu du message).
3. Transmission du message : Le serveur SMTP du destinataire reçoit le message, vérifie les informations et le transfère au système de messagerie approprié.
4. Confirmation : Le serveur SMTP envoie une réponse au client pour indiquer si le message a été accepté ou s'il y a eu des erreurs.

## Principes de sécurité dans le SMTP :&#x20;

Le SMTP a évolué pour inclure des mécanismes de sécurité tels que le STARTTLS, qui permet le chiffrement des communications SMTP via SSL/TLS. Cela garantit la confidentialité et l'intégrité des données pendant la transmission. De plus, le SMTP utilise des techniques de filtrage des spams pour identifier et bloquer les messages indésirables.

Le protocole SMTP joue un rôle crucial dans la transmission des e-mails et constitue la première étape pour acheminer les messages entre les utilisateurs. Comprendre son fonctionnement et ses principes de sécurité est essentiel pour garantir une livraison fiable des e-mails.
