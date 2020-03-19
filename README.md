# Deploy_Infra
Déploiement automatisé de l'infrastructure avec Terraform.

NB : main.tf.old correspond à notre ancien main.tf (avant l'organisation en modules).

## Organisation des fichiers
- DeployInfra-Jenkinsfile : code du pipeline de déploiement sur Jenkins
- main.tf et variables.tf : servent au lancement de Terraform. Main.tf s'appuie sur les modules suivants :
 - subnets
 - route_tables
 - nat 

Chaque module est composé de son propre main.tf & variables.tf. 
Un fichier output.tf permet de rendre la ressource disponible dans un autre module.
