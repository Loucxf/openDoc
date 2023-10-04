# Ajout d'un certificat ssl en local

Voilà une idée bien inutile mais bien pour comprendre les certificats SSL !



Comment ce forme un certificat et a quoi il sert :&#x20;

2 fichiers --> cert.crt (le certificat) + cert.key (la clé)



Certificat gratuit : let's encrypt



Sur débian :&#x20;

Installer snap&#x20;

```bash
sudo apt install snapd
```

Ajouter /etc/snap au PATH.

```bash
sudo snap install core
```

Installer certbot :&#x20;

```bash
sudo snap install --classic certbot
```

Générer le certificat et modifier la configuration apache :

```bash
sudo certbot --apache
```

Si ça ne marche pas :&#x20;

Modifie le path dans la configuration apache pour récupérer les fichiers de certificat\
Modifier le port apache par défault en 443 + ouvrir le port 443.&#x20;
