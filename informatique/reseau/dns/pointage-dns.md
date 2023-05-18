# 🪙 Pointage DNS

1. Enregistrement A (Address Record) : L'enregistrement A est utilisé pour lier un nom de domaine à une adresse IP IPv4 spécifique. Il s'agit de la forme la plus courante de pointage DNS et il permet de traduire un nom de domaine (par exemple, example.com) en une adresse IP (par exemple, 192.0.2.1). L'enregistrement A est utilisé pour diriger le trafic vers des serveurs Web, des serveurs de messagerie ou d'autres services accessibles via une adresse IP spécifique.
2. Enregistrement CNAME (Canonical Name) : L'enregistrement CNAME est utilisé pour créer un alias ou un pointeur vers un autre nom de domaine. Il permet de rediriger le trafic d'un nom de domaine vers un autre nom de domaine. Par exemple, si vous avez un enregistrement CNAME qui pointe de "[www.example.com](http://www.example.com)" vers "example.com", lorsque quelqu'un accède à "[www.example.com](http://www.example.com)", il sera redirigé vers "example.com". Les enregistrements CNAME sont souvent utilisés pour simplifier les configurations et les mises à jour en pointant vers des noms de domaine existants.
3. Enregistrement MX (Mail Exchanger) : L'enregistrement MX est utilisé pour spécifier les serveurs de messagerie qui doivent recevoir les e-mails destinés à un domaine spécifique. Lorsqu'un e-mail est envoyé à une adresse utilisant le nom de domaine spécifié, l'enregistrement MX indique les serveurs de messagerie responsables du traitement de ces e-mails. Les enregistrements MX permettent de diriger le trafic de messagerie vers les serveurs appropriés pour garantir une livraison efficace des e-mails.

Il existe de nombreux autres types d'enregistrements DNS, tels que les enregistrements TXT, les enregistrements AAAA pour les adresses IPv6, les enregistrements SRV pour les services spécifiques, etc. Chaque type d'enregistrement a un but spécifique et contribue à la configuration globale du système DNS pour un nom de domaine donné.