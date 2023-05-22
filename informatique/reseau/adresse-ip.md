# 📋 Adresse IP

## Adresses IP - réseau privé

Les adresses réservées à un usage de réseau privé sont définies par les spécifications de l'Internet Engineering Task Force (IETF) dans le document RFC 1918 intitulé "Address Allocation for Private Internets". Ce document établit les plages d'adresses IP qui sont réservées à un usage privé et ne sont pas routables sur Internet public.

Les plages d'adresses IP réservées pour les réseaux privés sont les suivantes :

* 10.0.0.0 à 10.255.255.255 (10.0.0.0/8)
* 172.16.0.0 à 172.31.255.255 (172.16.0.0/12)
* 192.168.0.0 à 192.168.255.255 (192.168.0.0/16)

Ces plages d'adresses IP peuvent être utilisées par les réseaux locaux internes pour les communications privées sans nécessiter d'enregistrement auprès d'une autorité centrale. Cependant, pour accéder à Internet avec ces adresses IP privées, un mécanisme de traduction d'adresse réseau (Network Address Translation - NAT) est généralement utilisé pour traduire les adresses privées en adresses publiques routables sur Internet.

Il est important de noter que l'utilisation de ces adresses IP privées est destinée aux réseaux locaux et ne doit pas être utilisée pour les communications publiques sur Internet.

## Adresses IP - réseau public



Une adresse IP publique est une adresse unique assignée à un appareil connecté à un réseau Internet. Elle permet d'identifier et de localiser cet appareil de manière unique sur Internet. Voici quelques points importants à connaître sur les adresses IP publiques :

1. Rôle de l'adresse IP publique : L'adresse IP publique est utilisée pour communiquer avec d'autres appareils et serveurs sur Internet. Elle est essentielle pour établir des connexions et échanger des données entre les appareils à travers le réseau mondial.
2. Adresses IP privées vs publiques : Dans un réseau local, chaque appareil possède également une adresse IP privée, qui est utilisée pour communiquer avec d'autres appareils au sein du même réseau local (par exemple, un réseau domestique ou un réseau d'entreprise). Les adresses IP privées ne sont pas routables sur Internet et sont utilisées pour organiser et gérer les appareils au sein du réseau local. Les routeurs effectuent une traduction d'adresse réseau (NAT) pour permettre aux appareils avec des adresses IP privées d'accéder à Internet via une adresse IP publique unique attribuée au routeur.
3. Attribution des adresses IP publiques : Les adresses IP publiques sont attribuées par des organisations centrales appelées registres Internet régionaux (RIR). Les RIR sont responsables de la distribution et de la gestion des plages d'adresses IP. Les fournisseurs d'accès Internet (FAI) et les grandes organisations obtiennent des blocs d'adresses IP auprès des RIR pour les allouer à leurs clients ou à leurs propres réseaux.
4. Notation de l'adresse IP publique : Une adresse IP publique est représentée sous la forme d'une suite de nombres séparés par des points, conformément au protocole IPv4 (par exemple, 192.0.2.1). Cependant, en raison de l'épuisement des adresses IPv4, le protocole IPv6 a été développé et utilise une notation différente qui permet un plus grand nombre d'adresses IP. Les adresses IPv6 sont généralement représentées sous la forme de huit groupes de quatre chiffres hexadécimaux, séparés par des deux-points (par exemple, 2001:0db8:85a3:0000:0000:8a2e:0370:7334).
5. Partage d'une adresse IP publique : En raison de la pénurie d'adresses IPv4, les fournisseurs d'accès Internet utilisent souvent des adresses IP publiques partagées via la technique de traduction d'adresse réseau (NAT). Cela signifie que plusieurs utilisateurs peuvent partager la même adresse IP publique, mais leurs connexions sont différenciées grâce à des numéros de port.

Les adresses IP publiques sont essentielles pour permettre la communication et la connectivité entre les appareils sur Internet. Elles jouent un rôle fondamental dans le routage des données et l'identification des appareils au sein du réseau mondial.

## Calcul du masque de sous-réseau

Le calcul du masque de sous-réseau est une étape essentielle dans la configuration des réseaux IP. Le masque de sous-réseau est utilisé pour délimiter la portion de l'adresse IP qui représente le réseau et la portion qui représente l'hôte. Voici comment calculer précisément le masque de sous-réseau :

2. Déterminer le nombre de sous-réseaux requis : Avant de calculer le masque de sous-réseau, il est important de connaître le nombre de sous-réseaux nécessaires dans le réseau global. Cela dépend des exigences spécifiques du réseau, du nombre d'appareils à connecter et de la répartition des adresses IP.
3. Convertir le nombre de sous-réseaux en une puissance de 2 : Le nombre de sous-réseaux requis doit être arrondi à la puissance de 2 supérieure la plus proche. Par exemple, si vous avez besoin de 6 sous-réseaux, vous devez arrondir à 8 (2^3).
4. Déterminer le nombre de bits de sous-réseau : Une fois que vous avez la puissance de 2, vous pouvez déterminer le nombre de bits nécessaires pour représenter les sous-réseaux. Ce nombre de bits sera ajouté au masque de la classe d'adresse IP existante.
5. Calculer le masque de sous-réseau : Pour calculer le masque de sous-réseau, vous devez convertir le nombre de bits de sous-réseau en une séquence binaire de 1 suivie de zéros pour compléter les 32 bits de l'adresse IP. Par exemple, si vous avez besoin de 3 bits de sous-réseau, vous obtenez 11100000 (ou 224 en décimal) pour le masque de sous-réseau.
6. Appliquer le masque de sous-réseau : Pour chaque adresse IP du réseau, vous appliquez le masque de sous-réseau en effectuant un "ET logique" entre le masque de sous-réseau et l'adresse IP. Cela permet d'obtenir l'adresse réseau correspondante.

Le masque de sous-réseau permet de diviser efficacement un réseau en sous-réseaux plus petits, ce qui facilite la gestion et la segmentation du trafic. En utilisant le calcul du masque de sous-réseau, vous pouvez définir des plages d'adresses IP spécifiques pour chaque sous-réseau et optimiser ainsi la configuration de votre réseau.
