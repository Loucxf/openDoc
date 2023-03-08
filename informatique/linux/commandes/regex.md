# 🐐 Regex

Les expressions régulières, ou "REGEX", sont des motifs de texte utilisés pour rechercher et manipuler des chaînes de caractères. Les REGEX sont couramment utilisées dans des langages de programmation, des outils de traitement de texte et des utilitaires en ligne de commande pour effectuer des opérations de recherche et de remplacement de texte.

Voici quelques exemples courants de REGEX :

* ^ : Représente le début de la chaîne. Par exemple, l'expression régulière "^Bonjour" recherchera toutes les chaînes commençant par "Bonjour".
* $ : Représente la fin de la chaîne. Par exemple, l'expression régulière "au revoir$" recherchera toutes les chaînes se terminant par "au revoir".
* . : Représente n'importe quel caractère. Par exemple, l'expression régulière "b.t" recherchera toutes les chaînes contenant un "b", suivi de n'importe quel caractère, suivi d'un "t" (par exemple, "bat", "bet", "but", etc.).
* \[.] : Représente une classe de caractères. Par exemple, l'expression régulière "\[aeiou]" recherchera toutes les chaînes contenant une voyelle (par exemple, "bonjour", "ami", etc.).
* \[^ ] : Représente une classe de caractères négative. Par exemple, l'expression régulière "\[^aeiou]" recherchera toutes les chaînes ne contenant pas de voyelle (par exemple, "bjr", "mnt", etc.).
* \*: Représente zéro ou plusieurs occurrences du caractère ou de la classe précédente. Par exemple, l'expression régulière "bo\*t" recherchera toutes les chaînes contenant un "b", suivi de zéro ou plusieurs "o", suivi d'un "t" (par exemple, "bt", "bot", "boot", "booot", etc.).
* \+ : Représente une ou plusieurs occurrences du caractère ou de la classe précédente. Par exemple, l'expression régulière "bo+t" recherchera toutes les chaînes contenant un "b", suivi d'au moins un "o", suivi d'un "t" (par exemple, "bot", "boot", "booot", etc.).
* ? : Représente zéro ou une occurrence du caractère ou de la classe précédente. Par exemple, l'expression régulière "colou?r" recherchera toutes les chaînes contenant "color" ou "colour".
* ( ) : Permet de grouper des expressions régulières. Par exemple, l'expression régulière "(bonjour)+, (monde)?" recherchera toutes les chaînes contenant une ou plusieurs occurrences de "bonjour", suivies éventuellement de "monde" (par exemple, "bonjour bonjour", "bonjour bonjour monde", etc.).
