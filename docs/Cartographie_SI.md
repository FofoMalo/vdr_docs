# Cartographie_SI
## Cahier des charges : Analyse du besoin 

### Introduction
La mairie de Val-de-Reuil, dans sa vision à long terme souhaite disposer d'une cartographie de son système d'information. Il n'existe actuellement pas en l'état un document, une méthode de ce genre permettant d'avoir une vue globale du système d'information.
L'état actuelle des lieux donne une vue suivante : 
il existe un (1) Responsable de la modernisation numérisque qui lui même travaille en étroite collaboration avec le Responsable de la Sécurité des Systèmes Informatique. 
Ce dernier porte également la casquette  d'administrateur des systèmes et du réseaux.
Il peut être assisté par un consultant extérieur pour ce qui est de la gestion des progiciels au compte de la mairie.
Une de mes tâches principale sera d'analyser et de comprendre le besoin, fournir une solution durable permettant à la ville de se munir d'un outil efficace, propriétaire et simple à utiliser.

Il existe un document élaborer par l'Agence Nationale de la Sécurité des Système d'information [Guide ANSSI](https://www.ssi.gouv.fr/guide/cartographie-du-systeme-dinformation/) additionné à la [Ebios risk manager](https://www.ssi.gouv.fr/entreprise/management-du-risque/la-methode-ebios-risk-manager/) qui donne une lecture de ce que devrait être une cartographie du SI.
Les Organismes d'importances Vitales (OIV) au sein d'un système d'information garantissent la continuité du SI. Leurs protections nécessitent une bonne lecture par les différents acteurs et responsables du système d'information. Une des raisons qui nécessite la mise en place d'une cartographie du SI est que lorsqu'il n'y a que quelques personnes qui connaissent le système d'information en soi cela peut être une faille de sécurité énorme pour l'organisme en question.

> Nul n'est à l'abri d'une erreur.

C'est pour cela que mettre en place une cartographie qui fera les connections nécessaires entre les différentes vues métiers, systèmes, et réseaux permettra de se munir d'outil efficace pour assurer une continuité des services, de par là favoriser une meilleur intégration des systèmes applicatifs au sein du système d'information.
En résumé, cette approche permettra à la ville et à ses responsables d'acquérir une maîtrise totale du système d'information. La mairie aura ainsi une connaissance exhaustive de tous les composants d'importance vitale du SI. Cette maîtrise se traduira par une meilleure protection du système d'information, car nous serons en mesure d'identifier plus précisément les systèmes les plus critiques et les plus exposés. De plus, cela renforcera la capacité de défense de la ville, car une connaissance approfondie du SI permettra de réagir de manière plus efficace en cas d'incident ou d'attaque. Enfin, cette approche favorisera la résilience en permettant de mettre en place un plan de continuité d'activité, qu'il soit numérisque ou non.
## Plan de travail : analyse du besoin 
Pour la réalisation de la cartographie j'ai mis en place une méthode de découpage de l'information au près des personnes ressources, cela a permis de dégager les étapes suivantes : 

**Collecte des informations** :

   - Réunir les documents existants sur l'infrastructure IT actuelle : Cette étape est cruciale et reste encore à parfaire, certaines données étant fortement sensible je n'ai pas eu accès.
   - Rencontrer les différents responsables de service pour obtenir des informations supplémentaires.

**Identification des composants du SI** :

   - Réseaux (LAN, WAN, VLAN).
   - Serveurs (physiques, virtuels).
   - Applications métiers (AxelNet, MobiliEcole).
   - Bases de données (MySQL, PostgreSQL).
   - Postes de travail (PC, tablettes).
   
**Représentation graphique** :

j'ai utilisé ==Xmind== (outil de mindmapping) pour créer une représentation visuelle du SI décomposée en : 

- Nœuds principaux : Réseaux LAN, WAN, VLAN, Serveurs (physiques, virtuels), Applications métiers (AxelNet, MobiliEcole), Bases de données (MySQL, PostgreSQL), Postes de travail (PC, tablettes).
- Sous-nœuds : détailler chaque composant en incluant des informations telles que les adresses IP, les versions logicielles, les interconnexions, etc.

**Relations et interconnexions** :

   - Identifier et représenter les liens entre les différents composants du SI.
   - L'utilisation des flèches de direction dans les tableaux donne une meilleur compréhension du flux de d'informations entre les données, les services et les composants du SI.

**Documentation complémentaire** :

   - L'ajout des notes et des commentaires pour fournir des explications supplémentaires sur certains éléments du SI.
   - j'ai inclu des informations sur la sécurité, la disponibilité et la performance de chaque composant selon les informations qui m'ont été fournies.

**Mise à jour régulière** :

   - Une planification des sessions de mise à jour régulières pour maintenir la cartographie du SI à jour avec les évolutions et les changements. J'éffectue pour cela un suivi sur les *issues github du code source*. S'assurer dans ce cas de bien lancer la commande de mise à jour de composer pour toutes les dépendances du projet avec la commande suivante :  `composer update`
   
**Partage et collaboration** :

   - Dans le plan de prise en main de l'outil de la cartographie, la gestion et les accès sont gérées par la définition des rôles :
1. L'administrateur : il a tout les droits. Il peut créer, modifier, attribuer de nouveaux rôle
2. Le Cartographe : il a des droits restreints sur les objets qu'il crée. Il n'a pas d'accès aux objets utilisateurs et configuration.
3. L'auditeur : a le droit d'accéder et d'afficher tous les objets exception faite des utilisateurs et de la configuration 
De nouveaux rôles peuvent être créer et définie selon les besoins de la municipalité.

**Utilisation de la cartographie du SI** :

   - La carte est une aide à la prise de décision en identifiant les points faibles et les opportunités d'amélioration du SI.
   - Elle se veut modératrice dans la communication et la compréhension entre les différents acteurs du SI.
   - Elle doit servir de référence lors de l'élaboration de nouvelles stratégies ou de nouveaux projets.

## Benchmark des communes ayant fait une cartographie de leur système d'information
je n'ai pas eu de référence dans mes recherches sur le net. Ce qui parait absolument censé car la cartographie représente l'ensemble du SI et donne une lecture globale pour qui comprend les aspects techniques. Ce qui m'a amené à me pencher d'avantage sur les différents outils disponibles pour créer une cartographie du SI.
#### Benchmark : Logiciels libres Architecture d'entreprise (AE)

|N°|Nom|description|Avantages|Inconvenients|Notes|
|:--|:---|:---------|:---------|:---------|:---------|
|1|[Modelio](https://www.modelio.org/)|modélisation de données|s'installe et se désinstalle facilement|Ne permet pas le partage entre plusieurs utilisateurs autorisés|testé |
|2|[Visual Paradigm](https://www.visual-paradigm.com)|Online|SAAS exclusif| Serveurs externes|testé |
|3|[ADOIT](https://www.boc-group.com/fr/adoit/get-started/)| solution payante| clé en main| gestion externe et coût|testé|
|4|[Arch Imatetool](https://www.archimatetool.com/)| excellent et opensource|gratuit puissant| courbe d'apprentissage|testé|
|5|[Draw.io](https://app.diagrams.net/)| hybride, locale et cloud|multiplateforme| Pas de prise en compte des recommendation ANSII|testé|
|6|[==Mercator==](https://github.com/dbarzin/mercator/tree/master)|Norme ISO27001:2013 utilisé par 15 centres hospitaliers 3 communes en France.|née d'un besoin spécifique, en lien avec les récommandations ANSII| Suivi des Mises à jour, veille obligatoire|utilisé|

## Les vues
Les vues sont progressives allant du métier vers la technique, elles mêmes déclinées en vues. Ainsi tous les acteurs qui seront reférencés peuvent avoir une lecture du SI. Les données peuvent être exportées sous plusieurs formats bureautique à des fins d'analyse. 
Formats disponibles : CSV, PDF, Excel.
Pour les besoins d'impression nous pouvons également définir les colonnes qui nous intéressent afin de les exploiter.
### Métiers : Services de la Commune

!!! info "Ecosystème"
    Vue d'ensemble : Processus => technologies utilisées => données produites => personnes (acteurs internes et ou externes)
    Vue métier du SI : Processus et informations clés qui sont nécessaires pour que le SI remplisse sa fonction = Valeurs Métiers

#### Tableau des Métiers : Vue Métier
!!! infor "Vue métier et granularité"
     niveau 1 : informations indispensables
     niveau 2 : informations importantes
     niveau 3 : informations utiles


| Nom   | Description                 | Responsable                      | @mail                    | granularité |
| :-----| :-------------------------- | :------------------------------- | :----------------------- | :--- |
| Finances                               | Administration et Finances  | Resp | @valdereuil.fr   | 1 |
| Ressources Humaines                    | Administration et Finance   | Resp | @valdereuil.fr  | 3|
| Centre Communal d'action social (CCAS) | Directions Opérationnelles  | Resp | @valdereuil.fr | 1 |
| Enfance-Jeunesse-et-emploi             | CCAS                        | Resp | @valdereuil.fr | 1 |

#### Tableau services : Vue Processus

!!! info "Vue Processus"
    j'ai commencé par décomposer la gestion de la paie :
    identifier les Besoins et processus utilisés pour effectuer la paie.

| Services                        | Processus                                                         | Logiciels |
| :------------------------------ | :---------------------------------------------------------------- | :-------- |
| Gestion des ressources humaines | -Paie -Carrière -Agents -Retraite -Congés                                     | x  |
| Enfance et Jeunesse             | Inscription -Revenus -Données sur la santé des enfants                        | x  |
| Tiers, Subvention Budget        | Données_Financières_et_Bancaires -Données_Personnelles -Données_Entreprises   | x  |

#### Tableau : Vue Application

!!! info "Vue applicative"
    Décrire les composants du logiciels du SI, des services offerts, et les flux de données entre eux.
    La vue de l'administration : Nous allons répertorier les périmètres et les niveaux de privilèges c'est à dire les types d'utilisateurs(Cartographe, auditeurs, utilisateurs) et admin du SI.

| Applications/Logiciels | Services A                          | Service B  | Données         |
| :--------------------- | :---------------------------------- | :--------- | :--------------- |
| Horoquartz -> 2        | Gestion des Ressources Humaines-> 3 | Finances 4 | <-temps/agents 1 |
|AxelNet -> TeamNet      | portail_famille->Enfance-jeunesse-Emploi hygiène|Finances|reservation, paiement, activités scolaires|

#### Tableau : Vue Infrastructure

!!! info "Vue Infrastructure"
   La vue des Infra Logiques : Cloisonnement logique des réseaux, la définition des plages d'adresses IP, les VLAN, WLAN,IPBX et les fonctions de filtrages utilisées sur les routeurs.
   La vue des Infra Physique : Description des équipements physiques utilisés par le SI

| Services                               | Plage @IP | Nom ou code VLAN | Equipements          | Licences      |
| :------------------------------------- | :-------- | :--------------- | :------------------- | :------------ |
| Finances                               |           | 1                | PC, Mac, Workstation | O365          |
| Ressources Humaines                    |           | 1                | PC, Workstation      |    |
| Centre Communal d'action social (CCAS) |           | 1                | PC, Workstation      |    |
| Enfance-Jeunesse-Petite Enfance CCAS   |           | 1                | PC, Workstation      |    |
| Services Informatiques                 |           |                  |Serveur physique : constructeur|      |


## Application : Mercator pour la cartographie du SI

Mercator est un outil open source permettant de mettre en place une cartographie du système d'information. Il respecte le guide mis en place par l'ANSSI et a été développé par ==Didier Barzin==. La dernière version est `Maturity 1c`. C'est l'outil qui répond le plus au besoin de la municipalité. L'historisque du développement du projet est assez similaire à celui de la ville de Val-de-Reuil. Un besoin d'avoir l'information précise de suivi et d'évolution du SI par une petite équipe pour un grand nombre de matériel, logiciel, et projet en cours.
Dans le cas de la mairie j'ai choisi un serveur [Fedora](https://fedoraproject.org/server/) car il est robuste et incorpore les fonctionnalités avant-gardistes dans l'univers des serveurs linux. Il est dérivé de RedHat, sa documentation est à jour et bien concise.  

### Prérequis

Avant de commencer, il faut s'assurer de disposer des éléments suivants :

- Un serveur de production avec les caractéristiques suivantes :
  - Système d'exploitation : Fedora Server 64 bits (un serveur dérivé de debian aussi peut parfaitement être mis en place)
  - RAM : 2 Go
  - Disque : 20 Go
  - VCPU : 2
### Installation
Installation et configuration d'un serveur fedora. La documentation officielle fournit une meilleur explication sur les différentes méthodes d'installation. Dans ce projet je travaille dans un environnement virtuelle sous Vmware workstation v16.
Ma configuration : 2Mo pour le Bios, 2 Go de swap, et 18 Go xfs sur la partition /.
### Mis à jour : Fedora Linux (OS)
Avant d'installer Mercator, je recommande fortement d'effectuer une mise à jour votre système en exécutant la commande suivante :

```bash
dnf update --refresh -y
```

### Installation des dépendances

Installez les dépendances nécessaires en exécutant les commandes suivantes :
Il s'agit pour l'essentiel de php, et d'un serveur web ici apache2.

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

J'installe Git, Graphviz et Composer; git pour le versionning, graphviz bibliothèque pour les vues et composer pour la gestion du site avec le framework Laravel.


[![asciicast](https://asciinema.org/a/QcMIjt4c46OETXphq7NcYdmYc.svg)](https://asciinema.org/a/QcMIjt4c46OETXphq7NcYdmYc)

```bash
dnf install git  graphviz composer -y
```

## Mise en route du projet

Avant de cloner le projet sous github je crée un dossier pour le projet de la cartographie nommer par mes soins le plus simplement du monde et lui accorder des droits.

```bash
cd /var/www && mkdir vdr_carto && chown $USER:$GROUP vdr_carto
```

Ensuite, je clone le projet Mercator depuis GitHub en exécutant la commande suivante :

[![asciicast](https://asciinema.org/a/pu73MJ9jL0aHtOam24B8l7A1K.svg)](https://asciinema.org/a/pu73MJ9jL0aHtOam24B8l7A1K)

```bash
git clone https://www.github.com/dbarzin/mercator /var/www/vdr_carto
```

Accédez au répertoire du projet Mercator :

```bash
cd /var/www/vdr_carto/mercator
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

Créez un fichier `.env` à la racine du projet Mercator en copiant le fichier `.env.example`  pour toutes les configurations ultérieurs nécessaire pour une connection à LDAP et SMTP :

```bash
cp .env.example .env
```

Modifiez le fichier `.env` pour y ajouter les informations de connexion à la base de données.
J'utilise comme éditeur de texte vim : `sudo vim .env`
```txt
## .env file
DB_CONNECTION=mysql
# DB_CONNECTION=pgsql.env si nous utilisons postgresql
# DB_HOST=127.0.0.1 si nous restons sur notre machine en locale
DB_HOST=@ipduserveurvirtuel
# pour des raisons de sécurité, nous devons changer le port de la base de données
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
Pour la première connection il faut utiliser les identifiants suivants : 

!!! important "username et password"
    - `admin@admin.com` 
    - `password`

Une fois connecté, vous pouvez commencer à remplir et administrer les données internes du système.
Pour des raisons évidentes de sécurité nous allons créer un nouvel admin, qui gérera les utilisateurs et la configuration du système. N'oubliez pas de bien supprimer celui de l'exemple.
Toutes les données seront rentrées manuellement, ce qui implique que chaque donnée collectée est bien maîtrisé avant son intégration dans la cartographie.

### Sécurité: Serveur et de la base de données

1. **Serveur** : 
Lister tous les services en cours d'exécution afin de déterminer les services qui ne sont pas utiles pour l'exécution de notre base de données afin de limiter les surfaces d'attaques.

```bash 
sudo dnf lsof -i
# lister les processus en cours d'exécution
sudo systemctl | grep running
# analyser et arrếter les processus qui ne sont pas utiles à l'éxécution du système
sudo systemctl stop bluetooth.service && sudo systemctl disable bluetooth.service

```
2. **Connection ssh**
Editer le fichier de configuration, changer le port d'accès ssh. Interdire la connection ssh via superuser (root). Il faut créer un utilisateur spécifique ou un group spécifique pour la connection au serveur.
Restreindre les accès à une plage d'adresse spécifique : `192.168.x.x dans le fichier etc/ssh/sshd_config`

3. **Préparer un cron pour la sauvegarde** :
J'ai mis en place un petit script pour les sauvegardes de la base de données.

!!! Important "mysql-dump priviliges"
     En lançant le script il peut y avoir un message d'erreur de connexion à la base de données pour réaliser le backup
     Solutions : reload & process

```mysql
GRANT RELOAD, PROCESS ON *.* TO 'vdr_admin'@'%';
# reload privilèges
FLUSH PRIVILEGES;
# pour voir la liset des utilisateurs et des hôtes 
select `User`, `HOST`, `Process_priv`, `Reload_priv` FROM mysql.user;

```


```bash
#!/bin/bash
# Configuration de la date pour le dossier de sauvegarde
NOW=$(date +%Y%m%d%H%M)
echo $NOW
backupDir="/home/fmalo/plan_de_sauvegarde/$NOW"

# Création d'un nouveau dossier avec la date
mkdir $backupDir

# Sauvegarde de la base de données MariaDB
mariadb-dump -u vdr_admin -pnu11pvdr -B mercator -x -e --lock-tables --flush-logs > "$backupDir/vdrcarto.sql" | gzip -9 "$backupDir/vdrcarto.sql.gz"
```

`crontab : 0 0 * * 1,5`
activer le cron avec la commande `crontab -e`

!!! info "Explication du script"
      Ce script bash effectue les opérations suivantes :
      Il génère une date au format "YYYYMMDDHHMM" et la stocke dans la variable NOW.
      Il crée un nouveau répertoire de sauvegarde avec le nom de la date générée.
      Il utilise la commande mariadb-dump pour sauvegarder la base de données "mercator" dans un fichier "vdrcarto.sql" situé dans le répertoire de sauvegarde.
      Il compresse le fichier "vdrcarto.sql" avec gzip, en obtenant "vdrcarto.sql.gz" dans le même répertoire de sauvegarde.
      Pour automatiser cette sauvegarde, j'ai configuré une tâche cron qui exécute ce script à 15 heures, les lundis et vendredis de chaque semaine.
## Modélisation: Système d'information
J'ai fait une modélisation préalable sous yED, sous la machine qui m'a été donné durant le stage. yEd est un logiciel puissant qui permet de la modélisation du système d'information.
Il n'en demeure pas moins qu'un outil comme mercartor répond mieux à toutes les préoccupations d'un responsable de la cartographie du SI.Mercator est bien plus qu'un outil d'inventaire il permet de comprendre les relations métiers et informatique de façon plus approfondie.
## Suivi et mise à jour du système : 
### git pull : mise à jour en locale depuis le dépôt distant
Dans le dossier var -> www -> vdr_carto lancer la commande `git pull` && `composer update`
cette tâche peut être automatiser dans un script. Dans le même état d'esprit nous pouvons affiner les rôles, cette tâche reviendra à l'administrateur.

## Comprendre la cartographie : IMPORTANT

### Règlement Général sur la Protection des Données (RGPD)
1. **Registre** : Dans cette section, nous explorons le registre RGPD en détail. Nous indiquons le nom du registre, sa description, le responsable du traitement, la finalité du traitement, les destinataires, la durée de rétention, le processus impliqué, les applications associées, et le cas échéant, nous chargeons un document référentiel 

2. **Mésure de sécurité** : Nous allons examiner ici les méthodes de suivis ou de vérifications de la conformité au RGPD qui ont été mises en place par les services responsables. L'implication du Délégué à la Protection des Données est capitale.
### Système d'information
1. **Macro-Processus** : Cette section vise à définir les macro-processus avec des noms explicites, en décrivant les éléments entrants et sortants. Indiquer les besoins de sécurité en tenant compte des indicateur suivants : le niveau de confidentialité, son niveau d'intégrité, son niveau de Disponibilité, et enfin le niveau de Traçabilité (==CIDT==). Il faut également définir un propriétaire qui peut être une entité/services, et lui attribué les processus découlant de la macro.

2. **Processus** : décrit l'activité soutenu par une ou plusieurs entités/Services. Il est important de situé les informations qui seront utiles dans le système d'information d'un point de vue granularité de l'information. il faut indiqué le ou les types d'activités, les applications soutenues c'est à dire celles qui soutiennent le processus. Identifier le type d'information traité par le processus ex: données bancaires, données personnelles. Nommer le responsable, et tagguer la macro. Définir les besoins de sécurité du processus. 

3. **Activités** : Il s'agit de nommer l'activité  de traitement, faire une description du traitement. Identifier le ou les processus lié(s). S'il existe des opérations en cours qui sont liés, nous les identifions.

4. **Informations** : Dans la cartographie l'information doit être identifiable, liée à un processus, avoir un propriétaire, un administrateur. Nous devons également indiquer son format de stockage, sa sensibilité, et ses besoins de sécurités du point de vue CIDT. S'il existe une contrainte réglementaire il faut le préciser et indiquer la norme en question
### Ecosystème
1. **Entités** : Indispensable pour la compréhension de la vue métier dans la cartographie, l'entité c'est ou le service qui participent à l'activité de traitement, manipulation des processus métiers en étroite lien avec les applications métiers identifiées. L'entité peut être interne ou externe. Nous l'identifions par son nom administratif, son niveau de sécurité, c'est à dire le type de maturité, le point de contact, le lieu de stockage des données manipulées par l'entité.

2. **Relations** : En définissant la nature de la relation qui existe entre les entités, que ce soit des biens, des servies, un partenariat commercial, nous avons une vue claire des différentes interactions qui donnent une lecture sur l'impact que peut avoir une application dans sa globalité. 
### Applications
1. **Bloc Applicatif** : Il s'agit d'identifier le fournisseur de l'application. 

2. **Applications** : Les applications métiers utilisées. il faut décrire l'écosystème de l'application : le responsable, le ou les entités qui utilisent l'application, nommé un référent fonctionnel, déterminer l'éditeur, le volume d'utilisateur de l'application, le cartographe (la personne qui renseigne l'application). Nous allons également exposer l'aspect technique de l'app. Définir le type de client c'est à dire cloud, web, on-premise, si l'app est un progiciel, en développement interne, son exposition à l'externe type de solution SAAS, ou autre. Il faut aussi pour un suivi et mis à jour de l'app indiquer la date d'installation, la date de la dernière mise à jour, la documentation technique. Identifier et indiquer la liste des services applicatifs délivrés par l'application, la liste des bases de données utilisées par l'application. Son niveau de sécurité d'un point de vue CIDT.
Très important c'est la possibilité de définir un plan de continuité et/ou de reprise d'activité Recovery time objective (RTO) et le Restart time objective. Du point de vue sécurité de l'app nous avons la possibilité d'uploader une base de données de CVE sur la plateforme. 
Voir les commandes suivantes:gc pour l'intégration d'une base disponible pour le common plateforme Enumeration [CPE](https:nvd.nist.gov/products/cpe) `gzip -d mercator_cpe.sql.gz` && `sudo mysql mercator < mercator_cpe.sql`.
Faire le lien avec le système d'information et l'infrastructure logique qui héberge la solution.
### Infrastructure logique
0. **Entités** : Point d'entrée globale
1. **Réseaux** : Nom du réseau identifié qui comportera une description, le type de protocole, le responsable de l'exploitation, le responsable de sécurité du système d'information, les besoins de sécurités (CIDT)
2. **Sous-réseaux** : Un nom pour identifier notre premier sous-reseaux, sa description, la plage d'adresse et le masque de sous réseaux, sa zone de parefeu, la passerelle par défaut, son appartenance à un Vlan, le type d'allocation (dynamique ou statique)+ la passerelle (NAT) son réseau de référence, préciser s'il accède au Wi-fi ou non. Si nous avons mis en place une zone démilitarisé nous allons également le spécifié. 
Une vue concise de l'infra logique dépendra de la description du réseau de l'entreprise, si elle n'est pas claire la gestion du risque de sécurité peut s'avérer délicate.

3. **Serveurs Logiques** : Établir la liste des serveurs logiques : Linux, Windows Server (année), hyperviseurs et Virtual Machines

4. **Routeurs** : Il faut spécifier le type de routeur, son nom, ses caractéristiques techniques et son adresse IP. Nous allons également préciser les règles de filtrages appliqués sur le routeur (gestion des Vlans)

5. **Commutateurs** : le nom de notre switch , sa drescription, son adresse ip, et ses caractérisque technique

6. **Vlan** : Il existera autant de vlan que nécessaire pour une meilleur gestion qui doit être représenter dans la cartograpgie. il faut indiquer l'ensemble des sous-réseaux qui le compose 

7. **Certificats** : la gestion des certificats permet d'envoyer à la personne responsable des certificats d'être prévenue dans les délais prévues pour prendre les mésures nécessaire. 
### Infrastructure Physique
1. **Sites** : Peut être le découpage géographie ou un découpage administratif, dans l'exemple de la municipalité il n'existe qu'un site physique c'est la ville. J'ai pris sur moi suite aux explications que j'ai reçu de part le RSSI de découper en deux sites : A -> B. A pour la gestion des Bâtiments connectés qui se situent sur plusieurs zones. B normalement devrait regroupé les bâtiments non encore connecté de la mairie. Ainsi si un bâtiment doit être connecté à l'avenir son plan d'intégration au réseau existant peut être facilement réalisé.

2. **Bâtiments/Salles** : L'ensemble des 8 bâtiments connectés identifiés dans la ville.

3. Postes de travail, Périphériques, Borne Wifi, Téléphones : il s'agit ici de faire l'inventaire de l'ensemble des équipements informatiques de la ville.
4. **Baies** : Serveurs physique, Commutateurs, stockage, Routeurs, Sécurité : idem réaliser l'inventaire exhaustif des acquisitions physique du matériel informatique. 

## Annnexes

### Reinstaller le projet sous un autre vmware-Workstation 
Dans le cadre de la suite de mon projet, j'ai été amené à copier la machine virtuelle sous un disque dur dans l'intention de le reinstaller.
La configuration de base, c'est à dire qu'il s'agisse du dimensionnement des disques ou de la configuration réseau n'ont pas posé de problème majeur.
La difficulté majeur rencontré fut un message d'erreur "the specified virtual disk need to be repaired", ce message fait echo à un précédent message d'erreur "failed to update autostart configuration". En effet j'étais sur une version 17 lors de mes tests, la version la plus récente, tandisque la version d'école est une 16 Pro.
**Solution** : 
Ensuite sous Windows 10 il faut réparer le disque de la machine virtuelle. 
Ouvrir le terminal `set-location C:\Programe File (x86)\Vmware\Vmware Workstation` -> lancer la commande suivante `.\vmware-vdiskmanager -R "C:\chemin\absolu\maMachineVirtuelle.vmdk`
Se rendre sur l'onglet de la machine virtuelle actuelle ==maMachineVirtuelle==, click droit -> se rendre sur `Manage` -> choisir `change hardware Compatibility` cloner la machine sans altérer l'existant, nommer la nouvelle machine et démarrer.

### Workflow : amelioration continue
- [x] Présentation PPTX
- [x] Documentation en ligne
- [x] Suivi et mis à jour du système
- [x] Backup Données (cron)
- [ ] Choisir les futurs cartographes
- [ ] Définir les auditeurs du système
- [ ] Formation et présentation au différents services (sensibilisation)
- [x] Veille Common vulnerabilities and exposures [cve-search](https://github.com/cve-search/cve-search)
- [ ] Backup vm
- [ ] Script pour la conservation et la suppression automatique des sauvegardes.
- [ ] Config : web server( Nginx)/ou Apache
- [ ] Générer un nouveau certificat, si non utilisé un certificat disponible: Transport Layer Secure/Secure Socket Layer connection (TLS/SSL).
