# Cartographie_SI
## Cahier des charges : Analyse du besoin, Introduction
La mairie de Val-de-Reuil, dans sa vision à long terme souhaite disposer d'une cartographie de son système d'information. Il n'existe actuellement pas en l'état un document, une méthode de ce genre permettant d'avoir une vue globale du système d'information.
L'état actuelle des lieux donne une vue suivante : il existe un 1. Le Responsable de la modernisation Numérique qui lui même travaille en étroite collaboration avec le Responsable de la Sécurité des Systèmes Informatique. Ce dernier porte également la casquette  d'administrateur des systèmes et du réseaux, Technicien.
Il est assisté par un consultant extérieur pour ce qui est de la gestion des progiciels au compte de la mairie.
Une de mes tâches principale sera d'analyser et de comprendre le besoin, fournir une solution durable permettant à la ville de se munir d'un outil efficace, propriétaire et simple à utiliser.

Il existe un document élaborer par l'Agence Nationale de la Sécurité des Système d'information (ANSSI) qui donne une lecture de ce que devrait être une cartographie du SI.
Les Organismes d'importances Vitales (OIV) au sein d'un système d'information garantissent la continuité du SI. Leurs protections nécessitent une bonne lecture par les différents acteurs et responsable du système d'information. Une nécessité de mettre en place une cartographie du SI est que lorsqu'il n'y a que quelques personnes qui connaissent le système d'information en soi peut être une faille de sécurité enorme pour l'organisme en question. 

> Nul n'est à l'abri d'une erreur.

C'est pour cela que mettre en place une cartographie qui fera les connections nécessaires des vues métiers, systèmes, réseaux permet de se munir d'outils éfficaces pour assurer une continuité des services, permettrent une meilleur intégration des système applicatifs au sein de l'environnement globale.
En somme la ville et ses responsables auront une maîtrise du système d'information, la mairie disposera d'une connaissance de l'ensemble des composants du SI. De la protection du système d'information; nous pourrions en effet mieux identifier les systèmes les plus critiques et les plus exposés. D'une défense car la connaissance du SI permettra réagir plus éfficacement en cas d'incident ou d'attaques. Et surtout une résilience mettre en place un plan de continuité d'activité numérique ou non. 

## Plan de travail : analyse 
Pour la réalisation de la cartographie les différentes étapes nous permettront d'atteindre nos objectifs : 

**Collecte des informations** :

   - Réunir les documents existants sur l'infrastructure IT actuelle.
   - Rencontrer les différents responsables de services pour obtenir des informations supplémentaires.

**Identification des composants du SI** :

   - Réseaux (LAN, WAN, VLAN).
   - Serveurs (physiques, virtuels).
   - Applications métiers (AxelNet, MobiliEcole).
   - Bases de données (MySQL, PostgreSQL).
   - Postes de travail (PC, tablettes).
   
**Représentation graphique** :

Utiliser un outil de mind mapping pour créer une représentation visuelle du SI.
   Nœuds principaux : Réseaux LAN, WAN, VLAN, Serveurs (physiques, virtuels), Applications métiers (AxelNet, MobiliEcole), Bases de données (MySQL, PostgreSQL), Postes de travail (PC, tablettes).
   Sous-nœuds : détailler chaque composant en incluant des informations telles que les adresses IP, les versions logicielles, les interconnexions, etc.
**Relations et interconnexions** :

   - Identifier et représenter les liens entre les différents composants du SI.
   - Utiliser des flèches pour indiquer les flux d'informations ou de données entre les composants.
**Documentation complémentaire** :

   - Ajouter des notes ou des commentaires pour fournir des explications supplémentaires sur certains éléments du SI.
   - Inclure des informations sur la sécurité, la disponibilité et la performance de chaque composant.
**Mise à jour régulière** :

   - Planifier des sessions de mise à jour régulières pour maintenir la cartographie du SI à jour avec les évolutions et les changements.
   
**Partage et collaboration** :

   - Utiliser un outil collaboratif pour permettre aux différentes parties prenantes d'accéder à la cartographie du SI et de contribuer aux mises à jour.
**Utilisation de la cartographie du SI** :

   - Aider à la prise de décision en identifiant les points faibles et les opportunités d'amélioration du SI.
   - Faciliter la communication et la compréhension entre les différents acteurs du SI.
   - Servir de référence lors de l'élaboration de nouvelles stratégies ou de nouveaux projets.

## Benchmark des communes ayant fait une cartographie de leur système d'information

#### Benchmark : Logiciels libres Architecture d'entreprise (AE)

|N°|Nom|lien|description|Avantages|Inconvenients|Notes|
|:--|:---|:---|:---------|:---------|:---------|:---------|
|1|Modelio|[lien vers le site](https://www.modelio.org/)|modélisation de données|s'installe et se désinstalle facilement|Ne permet pas le partage entre plusieurs utilisateurs autorisés|
|2|Visual Paradigm|[consulter le site](https://www.visual-paradigm.com)|Online|SAAS exclusif| Serveurs externes|
|3|ADOIT|[site](https://www.boc-group.com/fr/adoit/get-started/)| solution payante| clé en main| gestion externe et coût|
|4|Arch imatetool|[site](https://www.archimatetool.com/)| excellent et opensource|gratuit puissant| courbe d'apprentissage|
|5|Draw.io|[site_cloud](https://app.diagrams.net/)| hybride, locale et cloud|multiplateforme| Pas de prise en compte des recommendation ANSII|
|6|Mercator|[site_github](https://github.com/dbarzin/mercator/tree/master)|Norme ISO27001:2013 utilisé par 15 centres hospitaliers 3 communes en France.|née d'un besoin spécifique, en lien avec les récommandations ANSII| Suivi des Mises à jour, veille obligatoire|

## Les vues
### Métiers : Services de la Commune

!!! info "Ecosystème"
    Vue d'ensemble : Processus, technologies, données, personnes

    Vue métier du SI : Processus et information clés qui sont nécessaires pour que le SI remplisse sa fonction. "Valeurs Métiers"

#### Tableau des Métiers : Vue Métier

| Nom   | Description                 | Responsable                      | @mail                    | granularité |
| :-----| :-------------------------- | :------------------------------- | :----------------------- | :--- |
| Finances                               | Administration et Finances  | M G | @valdereuil.fr   | 1 |
| Ressources Humaines                    | Administration et Finance   | E B, M C | @valdereuil.fr  | 1|
| Centre Communal d'action social (CCAS) | Directions Opérationnelles  | S R | @valdereuil.fr | 1 |
| Enfance-Jeunesse-et-emploi             | CCAS                        | A D | @valdereuil.fr | 1 |

#### Tableau services : Vue Processus

!!! info "Vue Processus"
    Il me faudra commencer par décomposer la gestion de la paie :
    identifier les Besoins et processus utilisés pour effectuer la paie.

| Services                        | Processus                                                         | Logiciels |
| :------------------------------ | :---------------------------------------------------------------- | :-------- |
| Gestion des ressources humaines | -Paie -Carrière -Agents -Retraite -Congés                                     | x  |
| Enfance et Jeunesse             | Inscription -Revenus -Données sur la santé des enfants                        | x  |
| Tiers, Subvention Budget        | Données_Financières_et_Bancaires -Données_Personnelles -Données_Entreprises   | x  |

#### Tableau : Vue Application

!!! info "Vue applicative"
    Décrire les composants du logiciels du SI, des services offerts, et les flux de données entre eux.
    La vue de l'administration : Nous allons répertorier les périmètres et les niveaux de privilèges c'est à dire les  utilisateurs et admin du SI.

| Applications/Logiciels | Services A                          | Service B  | Données         |
| :--------------------- | :---------------------------------- | :--------- | :--------------- |
| Horoquartz -> 2        | Gestion des Ressources Humaines-> 3 | Finances 4 | <-temps/agents 1 |
|AxelNet -> TeamNet      | portail_famille->Enfance-jeunesse-Emploi hygiène|Finances|reservation, paiement, activités scolaires|

#### Tableau : Vue Infrastructure

!!! info "Vue Infrastructure"
   La vue des Infra Logiques : Cloisonnement logique des réseaux, la définition des plages d'adresses IP, les VLAN, WLAN,IPBX des fonctions de Filtrages
   La vue des Infra Physique : Description des équipements physiques utilisés par le SI

| Services                               | Plage @IP | Nom ou code VLAN | Equipements          | Licences      |
| :------------------------------------- | :-------- | :--------------- | :------------------- | :------------ |
| Finances                               |           | 1                | PC, Mac, Workstation | O365          |
| Ressources Humaines                    |           | 1                | PC, Workstation      | ...........   |
| Centre Communal d'action social (CCAS) |           | 1                | PC, Workstation      | ............. |
| Enfance-Jeunesse-Petite Enfance CCAS   |           | 1                | PC, Workstation      | ............. |
| Services Informatiques                 |xxxxxxxxxx|xxxxxxxxxxxxxxxxxxx|Serveur physique : constructeur|xxxxxxx|


## Mercator

Mercator est un outil open source permettant de mettre en place une cartographie du système d'information. Il respecte le guide mis en place par l'ANSSI et a été développé par Didier Barzin, RSSI. Je fais une veille actualisé depuis le dépôt github du projet. La dernière version est `Maturity 1c`. 

### Prérequis

Avant de commencer, assurez-vous de disposer des éléments suivants :

- Un serveur de production avec les caractéristiques suivantes :
  - Système d'exploitation : Fedora Server 64 bits
  - RAM : 2 Go
  - Disque : 20 Go
  - VCPU : 2

### Installation
Installation et configuration d'un serveur fedora. La documentation officielle fournit une meille explication sur les différentes méthodes d'installation. Dans ce projet je travaille dans un environnement virtuelle sous Vmware workstation v16.
### Mise à jour du système

Avant d'installer Mercator, mettez à jour votre système en exécutant la commande suivante :

```bash
dnf update --refresh -y
```

### Installation des dépendances

Installez les dépendances nécessaires en exécutant les commandes suivantes :

[![asciicast](https://asciinema.org/a/l5YssUIr0LHP75nVumpGGGkh9.svg)](https://asciinema.org/a/l5YssUIr0LHP75nVumpGGGkh9)

```bash
dnf install php-zip php-curl php-mbstring php-dom php-ldap php-soap php-xdebug php-gd php-fpm php-mysqlnd httpd
```

### Fedora : Service Apache 

Démarrez le service Apache et configurez-le pour qu'il démarre automatiquement au démarrage du système :

```bash
systemctl start httpd
systemctl enable httpd
```
### SGBDR : Installation de MariaDB

Installez MariaDB en exécutant la commande suivante :

```bash
dnf install mariadb-server
```

Démarrez le service MariaDB, vérifier et configurer pour qu'il démarre automatiquement au démarrage du système :

```bash
systemctl status mariadb
systemctl start mariadb
# Je vais rendre le service persistant grâce à la commande suivante : 
systemctl enable mariadb.service
```
### Installation de Git et Composer

J'installe Git, Graphiz et Composer, git pour le versionning, graphiz bibliothèque pour les vues et composer pour la gestion du site avec le framework Laravel,taper les commandes suivantes :


[![asciicast](https://asciinema.org/a/QcMIjt4c46OETXphq7NcYdmYc.svg)](https://asciinema.org/a/QcMIjt4c46OETXphq7NcYdmYc)

```bash
dnf install git  graphiz composer -y
```

## Mise en route du projet

Avant de cloner le projet sous github je vais créer un dossier pour le projet de la cartographie nommer par mes soins le plus simplement du monde et lui accorder des droits.

```bash
cd /var/www && mkdir vdrCarto && chown $USER:$GROUP vdrCarto
```

Ensuite Clonez le projet Mercator depuis GitHub en exécutant la commande suivante :

[![asciicast](https://asciinema.org/a/pu73MJ9jL0aHtOam24B8l7A1K.svg)](https://asciinema.org/a/pu73MJ9jL0aHtOam24B8l7A1K)

```bash
git clone https://www.github.com/dbarzin/mercator /var/www/vdrCarto
```

Accédez au répertoire du projet Mercator :

```bash
cd /var/www/vdCarto/mercator
```

Mettez à jour les dépendances de Composer en exécutant la commande suivante :

```bash
composer update
# au besoin 
composer require
```

Publiez tous les paquets depuis le gestionnaire des paquets de PHP en exécutant la commande suivante :

```bash
php artisan vendor:publish --all
```
## Configuration de la base de données
### Création de la base de données

Il faudrait se connecter afin de pouvoir mettre en place une base de données MySQL.
En tant qu'utilisateur root et créez une base de données pour Mercator :

!!! warning "Sécurité production"
      - Il faut créer un utilisateur, avec des droits administrateurs.
      - Les commandes et la connexion ssh se feront avec ce compte et non en root
      - Idem pour la gestion de la base de données.


```sql
mysql -u root -p

CREATE DATABASE mercator CHARACTER SET utf8 COLLATE utf8_general_ci;
CREATE USER 'vrd_user'@'localhost' IDENTIFIED BY 'xxxxxx';
GRANT ALL PRIVILEGES ON mercator.* TO 'vrd_user'@'localhost';
FLUSH PRIVILEGES;
EXIT;
```

[![asciicast](https://asciinema.org/a/7mUmtHSI4aDhbsDBNBGFGcyxw.svg)](https://asciinema.org/a/7mUmtHSI4aDhbsDBNBGFGcyxw)

### Configuration de Mercator

Créez un fichier `.env` à la racine du projet Mercator en copiant le fichier `.env.example` :

```bash
cp .env.example .env
```

Modifiez le fichier `.env` pour y ajouter les informations de connexion à la base de données.
J'utilise comme éditeur de texte vim : `vim .env`
```txt
## .env file
DB_CONNECTION=mysql
# DB_CONNECTION=pgsql.env si nous utilisons postgresql
# DB_HOST=127.0.0.1 : si nous restons sur notre machine en locale
DB_HOST=10.12.110.X 
DB_PORT=3306
# Comment DB_PORT for pgsql
DB_DATABASE=mercator
DB_USERNAME=vdr_user
DB_PASSWORD=xxxxxx

```

Exécutez les migrations pour créer les tables de la base de données :

```bash
php artisan migrate --seed
```

Générez une clé d'application en exécutant la commande suivante :

```bash
php artisan key:generate
```

Nettoyez le cache des configurations en exécutant la commande suivante :

```bash
php artisan config:clear
```

## Démarrage du serveur web

Démarrez le serveur web en exécutant la commande suivante :

```bash
php artisan serve -d
# Dans mon exemple en virtuelle pour accéder à l'hôte depuis mon addresse il faut lancer la commande suivante 
php artisan server --host 10.110.XX.XXX --port 8000
```

Vous pouvez maintenant accéder à l'application depuis votre navigateur à l'adresse [http://localhost:8000](http://localhost:8000). Sinon en virtuelle comme dans mon cas de figure sur l'adresse de votre hôte virtuel sur le port 8000.

## Prise en main
Pour la première connection important : 
!!! important "username et password"
    - `admin@admin.com` 
    - `password`

Une fois connecté, vous pouvez commencer à remplir et administrer les données internes du système.
Pour des raisons évidentes de sécurité nous allons créer un admin, et gérer ses droits. N'oubliez pas de bien supprimer celui de l'exemple.

### Sécurité: Serveur et de la base de données

1- Serveur : 
Lister tous les services en cours d'exécution afin de déterminer les services qui ne sont pas utiles pour l'exécution de notre base de données afin de limiter les surfaces d'attaques.

```bash 
sudo dnf lsof -i
# lister les processus en cours d'exécution
sudo systemctl | grep running
# analyser et arrếter les processus qui ne sont pas utiles à l'éxécution
sudo systemctl stop bluetooth.service && sudo systemctl disable bluetooth.service

```
2- Connection ssh
Editer le fichier de configuration, changer le port d'accès ssh. Interdire la connection ssh via superuser (root). Il faut créer un utilisateur spécifique ou un group spécifique pour la connection au serveur.
Restreindre les accès à une plage d'adresse spécifique : `192.168.x.x dans le fichier etc/ssh/sshd_config`

## Composition de la vue du système d'informations
J'ai fait une modélisation préalable sous yED, sous la machine qui m'a été donné durant le stage. yEd est un logiciel puissant qui permet de la modélisation du système d'information.
Il n'en demeure pas moins qu'un outil comme mercartor répond mieux à toutes les préoccupations d'un responsable de la cartographie du SI. Dans un sens l'outil est née d'un réel besoin de constat de sous effectif, d'un besoin de la compréhension globale du SI, plus qu'un inventaire il permet de comprendre les relations métiers et informatique.
