# 🍧 Serveur varnish

La fonctionnalité principale d'un serveur Varnish est de fournir une mise en cache HTTP réversible et rapide. Varnish est un serveur proxy de cache HTTP qui s'intercale entre le client et le serveur d'origine (backend) pour stocker en mémoire cache les réponses des requêtes HTTP.

Voici quelques fonctionnalités clés de Varnish :

1. Mise en cache : Varnish conserve en mémoire cache les réponses aux requêtes HTTP afin de répondre plus rapidement aux requêtes ultérieures. Cela réduit la charge sur le serveur d'origine et améliore les performances en fournissant des réponses plus rapides aux clients.
2. Purge de cache : Varnish permet d'effectuer des purges de cache pour invalider les éléments mis en cache et garantir que les clients reçoivent toujours les données les plus récentes lorsque cela est nécessaire. Les purges peuvent être effectuées manuellement ou automatisées selon les besoins.
3. Stratégies de mise en cache flexibles : Varnish offre une flexibilité pour configurer des règles de mise en cache basées sur des critères tels que l'URL, les en-têtes HTTP, les cookies, etc. Cela permet de définir des stratégies de cache adaptées aux besoins spécifiques de l'application.
4. Configuration avancée : Varnish offre une grande souplesse de configuration avec son propre langage de configuration appelé VCL (Varnish Configuration Language). Cela permet de personnaliser le comportement de mise en cache et d'effectuer des opérations avancées telles que la manipulation des en-têtes HTTP, la réécriture d'URL, etc.
5. Gestion de charge : En mettant en cache les réponses et en réduisant la charge sur les serveurs d'origine, Varnish contribue à améliorer la capacité de gestion de charge du système en permettant à un serveur de traiter davantage de requêtes sans nécessiter l'ajout de matériel supplémentaire.

En résumé, Varnish est utilisé pour accélérer la distribution de contenu en mettant en cache les réponses HTTP, réduisant ainsi la charge sur les serveurs d'origine et améliorant les performances globales du système.
