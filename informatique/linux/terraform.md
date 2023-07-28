# 🦖 Terraform

Terraform est un outil open source développé par HashiCorp qui permet de gérer l'infrastructure de manière déclarative. Il fait partie des outils d'Infrastructure as Code (IaC), ce qui signifie qu'il permet de décrire et de provisionner l'infrastructure de manière reproductible à l'aide de fichiers de configuration.

Voici les principaux concepts et fonctionnalités de Terraform :

1. Fichiers de configuration : Les configurations Terraform sont écrites dans un langage de description déclaratif appelé HashiCorp Configuration Language (HCL) ou en JSON. Les fichiers de configuration décrivent l'état souhaité de l'infrastructure, y compris les ressources, les fournisseurs, les variables, etc.
2. Déclaration des ressources : Dans Terraform, vous déclarez les ressources que vous souhaitez provisionner, telles que des machines virtuelles, des réseaux, des bases de données, des pare-feu, etc. Ces ressources sont définies en utilisant les modules fournis par les fournisseurs cloud (AWS, Azure, GCP, etc.) ou les modules personnalisés.
3. État de Terraform : Terraform maintient un état (state) qui stocke les informations sur l'infrastructure déployée. Cet état est stocké localement ou dans un backend distant, et il est utilisé pour gérer les modifications apportées à l'infrastructure au fil du temps.
4. Commandes Terraform : Terraform propose un ensemble de commandes pour gérer l'infrastructure. Parmi les commandes courantes, on trouve :
   * `terraform init` : Initialise un nouveau projet Terraform en téléchargeant les dépendances et en configurant le backend.
   * `terraform plan` : Affiche un plan détaillé des actions que Terraform effectuera pour atteindre l'état souhaité.
   * `terraform apply` : Applique les changements définis dans les fichiers de configuration et provisionne l'infrastructure en conséquence.
   * `terraform destroy` : Détruit l'infrastructure provisionnée précédemment.
   * `terraform state` : Gère l'état de Terraform, notamment en important et en exportant l'état.
5. Modules Terraform : Les modules Terraform permettent de regrouper et de réutiliser des configurations Terraform. Ils facilitent la gestion de configurations complexes et favorisent la modularité. Les modules peuvent être utilisés localement ou téléchargés depuis le registre Terraform.
6. Providers Terraform : Les fournisseurs (providers) sont des plugins qui permettent à Terraform de provisionner et de gérer des ressources spécifiques à un cloud ou à un fournisseur de services. Chaque fournisseur a ses propres ressources et fonctionnalités prises en charge par Terraform.

Terraform offre de nombreux avantages, notamment la gestion de l'infrastructure en tant que code, la reproductibilité, la possibilité de gérer des ressources multi-cloud, le suivi des modifications et la collaboration. Il est largement utilisé dans les environnements cloud et l'automatisation de l'infrastructure pour simplifier le déploiement et la gestion des ressources.
