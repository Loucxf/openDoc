# 🏈 Ansible

Ansible est une plateforme open-source d'automatisation et de gestion de la configuration qui permet de déployer, de configurer et de gérer des infrastructures et des applications de manière efficace et reproductible. Il utilise un langage déclaratif simple pour décrire l'état souhaité de votre système et effectue les tâches nécessaires pour atteindre cet état.

Voici quelques concepts clés d'Ansible :

1. Inventaire : L'inventaire d'Ansible est un fichier qui répertorie les hôtes (machines) sur lesquels vous souhaitez exécuter des actions. Il peut s'agir d'adresses IP, de noms de domaine ou de noms d'hôte. L'inventaire peut être organisé en groupes pour faciliter la gestion.
2. Playbooks : Les playbooks sont des fichiers YAML qui décrivent les tâches à exécuter sur un ensemble d'hôtes spécifiés dans l'inventaire. Les playbooks définissent les rôles, les tâches, les variables et les conditions pour effectuer une configuration ou une opération spécifique.
3. Rôles : Les rôles sont des ensembles de tâches, de fichiers de configuration, de modèles et d'autres ressources regroupés de manière logique et réutilisable. Ils facilitent l'organisation et la réutilisation du code Ansible en le divisant en modules autonomes et modulaires.
4. Tâches : Les tâches sont les actions à effectuer sur les hôtes. Elles peuvent inclure l'exécution de commandes, la copie de fichiers, la gestion des paquets, la configuration des services, etc.
5. Modules : Ansible dispose d'une vaste bibliothèque de modules qui permettent d'effectuer différentes actions sur les hôtes. Les modules sont des scripts exécutés sur les hôtes cibles et fournissent une interface simplifiée pour les opérations courantes. Par exemple, le module "copy" copie des fichiers sur les hôtes, le module "apt" gère les paquets sur les systèmes basés sur Debian, etc.
6. Ad-hoc Commands : Ansible permet également d'exécuter des commandes ad-hoc directement à partir de la ligne de commande sans utiliser de playbooks. Cela peut être utile pour effectuer des tâches ponctuelles ou pour vérifier rapidement l'état d'un hôte.
7. Configuration SSH : Ansible utilise SSH pour se connecter aux hôtes cibles et exécuter les tâches. Vous devez donc vous assurer que votre système de gestion Ansible peut se connecter aux hôtes cibles via SSH et que les clés SSH appropriées sont configurées.

Pour installer Ansible sur Debian, vous pouvez exécuter la commande suivante dans le terminal :

```sql
sudo apt update
sudo apt install ansible
```

Une fois Ansible installé, vous pouvez commencer à créer des playbooks et à exécuter des tâches sur vos hôtes cibles en utilisant la syntaxe YAML pour décrire les actions souhaitées.

Voici un exemple simple de playbook Ansible qui installe Apache sur un groupe d'hôtes spécifié dans l'inventaire :

```yaml
---
- name: Install Apache
  hosts: web_servers
  become: yes

  tasks:
    - name: Install Apache
      apt:
        name: apache2
        state: present
```

Ce playbook spécifie qu'il doit être exécuté sur le groupe d'hôtes "web\_servers" et qu'il doit installer le paquet Apache "apache2" en utilisant le module "apt".

Vous pouvez exécuter ce playbook en utilisant la commande suivante :

```bash
ansible-playbook -i inventory.ini install_apache.yml
```

L'inventaire (inventory) d'Ansible est un fichier ou un ensemble de fichiers qui spécifie les cibles de déploiement pour les opérations d'Ansible, y compris les serveurs distants, les groupes de serveurs et les variables associées.

Par défaut, le fichier d'inventaire est nommé "hosts" et se trouve généralement dans le répertoire `/etc/ansible/`. Cependant, vous pouvez spécifier un autre fichier d'inventaire lors de l'exécution d'Ansible en utilisant l'option `-i` ou `--inventory-file` suivi du chemin vers votre fichier d'inventaire personnalisé.

Le fichier d'inventaire peut être écrit au format INI ou YAML, et il permet de spécifier les adresses IP ou les noms d'hôte des serveurs cibles, les groupes auxquels ils appartiennent, les variables spécifiques à chaque serveur ou groupe, etc. L'inventaire offre une flexibilité pour organiser et gérer les serveurs sur lesquels les tâches Ansible seront exécutées.
