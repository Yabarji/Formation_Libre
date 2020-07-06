# Formation_Libre

# Projet Libre Dawan

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

## Projet Perso DAWAN
##### Objectif :
Obtenir avec un outil ou plusieur une architecture MVC démontable et ré-instable facilement et scalable.

Faire avec vagrant et ansible une configuration de serveur
##### Une architecture MVC
    1. un serveur frontend pour installer Nginx
        a. un partage pour le frontend qui se trouve sur un serveur DATA frontend ou partage NAS
    2. un serveur backend pour installer Apache et eclipse
        b. un partage pour le backend qui se trouve sur un serveur DATA backend ou partage NAS

    3. serveur DATA avec MySQL
    4. serveur DATA NoSQL
    
## Les étapes:
    Etape 1 : préparer le script Vagrant
    Etape 2 : préparer le script Ansible

#### Comparer les 2 cas 
Vagrant lance Ansible 
Ansible lance Vagrant

#### Terraform
Comparaison entre vagrant et terraform.

#### Les réseaux
Les 4 machines sont sur des réseaux différents
    - le front est exposé au réseau public
    - le backend est privé uniquement au frontend
    - les DATA sont privé uniquement au backend
    - les NAS sont privé (configuration dans un fichier facilement adaptable pour chaque utilisateur : l’utilisateur indique le PATH de ses fichiers)

#### Les environnements
    - Développement
    - Production
