# CICD_TP_Deploy_Infra


<div align="center">
  <img src="https://blog.sitm.ac.in/wp-content/uploads/2019/09/devops-660x330.png" width="210" height="110"/>
  <br>
  <br>
</div>



[![forthebadge](https://forthebadge.com/images/badges/uses-git.svg)](https://forthebadge.com)

<table>
<tr>
<td>
Dans le cadre d'un projet qui suit l'approche DevOps on réalise le déploiement d'une application.
Pour cela on utilise la plateforme d'intégration continu Jenkins.  

Ici ce dépot contient le fichier DeployInfra.tf. 
</td>
</tr>
</table>


## Sommaire

- [Prérequis](#prérequis)
- [Terraform](#Terraform)
- Le fichier
- Lien


## Prérequis

- Jenkins

On utilise Jenkins dans la version 1.5.1

```sh
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add - 
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list' 
sudo apt update 
sudo apt install default-jre jenkins --yes 
sudo systemctl enable jenkins 
sudo systemctl start jenkins 
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

- Compte AWS (+création d'un rôle)

On utilise le fournisseur de Cloud AWS. On créer un rôle pour que le fichier Packer puisse interagir avec l’API AWS. 

## Terraform

On utilise Terraform (dans la version 12.20) pour déployer de manière automatisé. Terraform à l’avantage d’être Cloud agnostique c’est-à-dire indépendant du Cloud Provider.

## Le fichier 

Le fichier DeployInfra.tf sera utilisé pour créer notre infrastructure (VPC, subnet ...).

## Lien 

[(Back to top)](#sommaire)

Voici ci-dessous quelques liens de dépot à consulter pour avoir plus d'information sur le déploiement.

- Liens :
  - https://github.com/birintha/CICD_TP_Build_AMI 
  - https://github.com/birintha/CICD_TP_Deploy_WebApp


