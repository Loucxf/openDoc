# 🔁 NAT | PAT

La traduction d'adresse, également connue sous le nom de Network Address Translation (NAT), est une technique utilisée dans les réseaux informatiques pour traduire les adresses IP d'un réseau à un autre. Elle est principalement utilisée pour permettre à plusieurs appareils d'un réseau privé d'accéder à Internet en partageant une seule adresse IP publique routable.

Lorsqu'un réseau privé utilise des adresses IP privées (par exemple, dans la plage 192.168.0.0/16), ces adresses ne sont pas routables sur Internet public. Afin de permettre aux appareils de ce réseau privé de communiquer avec des ressources sur Internet, une traduction d'adresse est effectuée par un dispositif de traduction d'adresse réseau, généralement un routeur.

Le dispositif NAT attribue une adresse IP publique routable au trafic sortant provenant des appareils du réseau privé. Lorsque les réponses reviennent, il effectue la traduction inverse en remplaçant l'adresse IP publique par l'adresse IP privée appropriée de l'appareil destinataire. Ainsi, les appareils du réseau privé peuvent partager une seule adresse IP publique pour accéder à Internet.

La traduction d'adresse est couramment utilisée dans les réseaux domestiques, les réseaux d'entreprises et les fournisseurs de services Internet (ISP) pour économiser des adresses IP publiques et permettre une connectivité Internet pour de nombreux appareils à partir d'une seule adresse IP.

Le Port Address Translation (PAT) est une variante de la traduction d'adresse réseau (NAT) qui permet de traduire non seulement les adresses IP, mais également les ports TCP ou UDP. Le PAT est également connu sous d'autres noms tels que NAT overload, NAT masquerading ou IP masquerading.

Dans le contexte du PAT, chaque appareil du réseau privé se voit attribuer une adresse IP privée unique, mais tous les appareils partagent une seule adresse IP publique routable. La traduction se fait en utilisant des ports TCP ou UDP spécifiques associés à chaque connexion.

Lorsqu'un appareil du réseau privé établit une connexion avec un serveur sur Internet, le dispositif de PAT (généralement un routeur) modifie l'adresse IP source de l'appareil en remplaçant l'adresse IP privée par l'adresse IP publique et assigne un port spécifique à cette connexion. Lorsque la réponse du serveur est reçue, le dispositif PAT utilise les informations du port pour rediriger la réponse vers l'appareil approprié dans le réseau privé.

Le PAT est utilisé dans les cas où plusieurs appareils d'un réseau privé doivent partager une seule adresse IP publique routable pour accéder à Internet. Il permet d'économiser des adresses IP publiques en utilisant des ports pour différencier les connexions provenant de différents appareils. Cela permet à plusieurs utilisateurs d'un même réseau privé d'établir des connexions simultanées avec Internet en utilisant un seul point d'accès à Internet.

Le PAT est couramment utilisé dans les réseaux domestiques, les petites entreprises et les environnements où il y a un grand nombre d'appareils qui nécessitent une connectivité Internet, mais où les adresses IP publiques sont limitées.

Pour aller plus loin :&#x20;

1. NAT statique : Dans le NAT statique, une adresse IP privée spécifique est associée à une adresse IP publique spécifique de manière permanente. Cela permet d'établir une correspondance un-à-un entre les adresses IP privées et publiques, sans utiliser de ports pour la traduction.
2. NAT dynamique : Le NAT dynamique est similaire au PAT, où une seule adresse IP publique est partagée par plusieurs adresses IP privées. Cependant, contrairement au PAT qui utilise des ports, le NAT dynamique utilise une table de traduction pour associer dynamiquement les adresses IP privées aux adresses IP publiques disponibles.
3. NAT bidirectionnel : Le NAT bidirectionnel permet la traduction des adresses IP et des ports à la fois pour les connexions sortantes et entrantes. Cela permet de gérer les connexions initiales établies à partir du réseau privé et les réponses correspondantes provenant d'Internet.
4. NAT virtuel : Le NAT virtuel (Virtual NAT) est utilisé dans les environnements de virtualisation où plusieurs machines virtuelles partagent une seule adresse IP publique. Il permet de traduire les adresses IP et les ports des machines virtuelles pour accéder à Internet.

Ces différentes techniques de traduction d'adresses sont utilisées pour permettre la connectivité entre les réseaux privés et Internet, en économisant les adresses IP publiques, en améliorant la sécurité du réseau et en facilitant la gestion des communications réseau. Le choix de la technique appropriée dépend des besoins spécifiques du réseau et de la configuration mise en place.
