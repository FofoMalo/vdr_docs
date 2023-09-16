# Feuille de route

## 1. Cartographie du système d'information de la ville de Val-de-Reuil

### Date : 17 Juillet au 22 Septembre 2023

### Topic

### Notes

## 2. - Objectif : Visualiser et comprendre l'ensemble des composants et des interconnexions du système d'information de la Mairie de Val de Reuil

### Main Points

### Examples

### Details

## 3. Mon organisation interne

### Orga_Cartograhie

-  Collecte des informations

	- Réunir les documents existants sur l'infrastructure IT actuelle

	- Rencontrer les différents responsables de services pour obtenir des informations supplémentaires

- Identification des composants du SI

	- Réseaux (LAN, WAN, VLAN)

	- Serveurs (physiques, virtuels)

	- Applications métiers (AxelNet, MobiliEcole)

	- Bases de données (MySQL, PostgreSQL)

	- Postes de travail (PC, tablettes)

- Representation graphique

	- Utiliser un outil de mind mapping pour créer une représentation visuelle du SI

		-  Nœuds principaux : Réseaux, Serveurs, Applications, Bases de données, Postes de travail 

		- Sous-nœuds : détailler chaque composant en incluant des informations telles que les adresses IP, les versions logicielles, les interconnexions.


- Relations et interconnexions

	- Identifier et représenter les liens entre les différents composants du SI

		- Utiliser des flèches pour indiquer les flux d'informations ou de données entre les composants

- Documentation complémentaire

	- Ajouter des notes ou des commentaires pour fournir des explications supplémentaires sur certains éléments du SI

		- Inclure des informations sur la sécurité, la disponibilité et la performance de chaque composant

- Mise à jour régulière

	- Planifier des sessions de mise à jour régulières pour maintenir la cartographie du SI à jour avec les évolutions et les changements

- Partage et collaboration

	- Utiliser un outil collaboratif pour permettre aux différentes parties prenantes d'accéder à la cartographie du SI et de contribuer aux mises à jour

- Utilisation de la cartographie

	- - Aider à la prise de décision en identifiant les points faibles et les opportunités d'amélioration du SI

		- Faciliter la communication et la compréhension entre les différents acteurs du SI

			- Servir de référence lors de l'élaboration de nouvelles stratégies ou de nouveaux projets

### Orga_Intranet

### Orga_Open_data

### Orga_Recommandations_RGPD

### Orga_Accessibilité_site_VDR

### Orga_Cyber_Secu

- Logiciels_a_utiliser

	- Pour la Sécurité

		- [OpenVAS(Greenbone)](https://github.com/greenbone)

	- Pour le Réseau

		- Nmap

		- ELK Stak

	- Pour le Système d'opération

		- [Ping Castle](https://www.pingcastle.com/)

		- [purpleKnigth](https://purple-knight.com/)

	- Recommandations utilisation de keepassxc

		- [Voir logiciels recommandés ANSII](https://code.gouv.fr/sill/list)

## Dossier Projet M2I

### Plan

### ressources

### redaction

- introduction

- préambule

- Dossier

### Kanban_project

## Architecture_physique

### Fournisseur d'accès Internet

- Orange

- VDR_juridiquement_RGPD

- Fibre optique

### Câblage réseau

- RJ45 Cat6

  Cat-6A : vitesse de transmission 10Go/s sur la base de la norme ethernet 10G BASE-T.
  Résitance : 500Mhz
  Compatible avec les normes PoE, et PoE+
  
- Description technique :


  Forte résistance aux interférences électromagnétiques
  Fréquences : 250Mhz (Résistance)
  Long max : 100m
  Plus de bande passante aux appareils
  Retro-Compatibilité
  Débit autorisé : 1Go/s
  
### Baie Informatique : 8

- Médiathèque

- Espage

- Piscine

- Mairie

- Police Municipale

- Sport:salle couverte jesseOwen

- Centre technique Municipale

- A complèter : CCAS jacques mono

### Routeurs :

- Modèle : Coeur de réseau
Nombre : 2

  Il fourni une bande passante maximale pour connecter des routeurs, ou des commutateurs supplémentaires.
  Deux bâtiments : Centre Technique Municipal et Mairie.
  2 Routeurs coeur de réseaux.
  Hpe-Aruba probalement
  
- Routeurs périphériques/Distributions : 7

- durée de vie :

### Onduleurs :

- HPE integrated lights-Out (ILO)

### Switchs

Modèle probable : HPE Aruba 2530 : 
Fonctionnalités avancées de routage et de commutation
48 ports Gigabit ethernet
Type 2
PoE (Power over Ethernet)
Besoins : Au moins 160 ports, les téléphones pouvant être mis en vlan donc utiliserons le même port avec une séparation logique (VLAN) tagged
Administation 10
Utilisateurs 20
Serveurs 30
Téléphonie 40
Wifi invité 40
---Nomenclature
sw_10_Bt1_48_2_@ip
(switch vlan10 Batiment 1 48 port type2 dernière @ip)
---Lien fiche technique sur le site officiel
https://www.arubanetworks.com/assets/ds/DS_2530SwitchSeries.pdf

### Téléphonie

- Protocole : IPBX

  Internet Protocol Private branch exchange
  VOIP : voice over internet protocol , utilisé dans ce cas pour un standard téléphonique via réseaux IP.
  Il est connecté au switch
  
	- Phones : 250 

### WI-FI

## Architecture_logique

### Réseaux

Réseaux : NET-ADDRESSE : 192.168.10
	  HOST-ADDRESSE : 10
 192.168.10.0/
Masque : 255.255.255.0

- VLAN

- VPN

  Fortigate : 
  Solution propriétaire de fortinet, incluant plusieurs fonctionnalités de gestion des parefeu, vpn, et des solutions AccèsZeroTrust, proxy.
  
- Sous-réseaux

  Le sous reseau est en base 24, pour l'addressage locale
  192.168.1.0/24
  Exple : 192.168.10.0/24 254 PC
  192.168.20.0/24  254 PC 
  192.168.30.0/24  254 PC
  192.168.40.0/24  254 PC
  
  
### Serveurs

- Physiques

  informations requises pour le SI : Marque fabriquant et nom du srv: 
  Le système d'exploitation
  Memoire CPU
  Ram
  Disque
  Dique utilisé
  Date d'installation
  Date de mise à jour
  Responsable 
  @ip du srv-phy
  Site
  Bât
  Baie
  
	- Active Directorie

	- DHCP

	- DNS

- Virtuelles

	- VmWare

		- ESXI7

			- Vcenter

	- Hyper-V

### Sécurité

- FortiClientVPN

  version: 7.0.3.0193
  
- Remote_controle

	- TightVNC

	  Virtual Network Computing : C'est la solution utilisée actuellement par l'équipe Informatique.
	  Installé sur les hotes client
	  
	  
	- TeamViewer

- Anti-virus

	- Kaspersky

- Monitoring

	- Simplivity

- PowerShell _Audit_Password

  # Il faut commencer par installer le module  : DSInternals depuis le store powershell
  
  $domain = "dc=valdereuil, dc=local"
  $dc = "srv-dc"
  $dico = "c:\datafiletocheck"
  get-ADReplAccount -All -server $dc -NamingContext $domain | Test-PasswordQuality -WeakPasswordsFile $dico -IncludeDisableAccounts
  # Bien s'assurer que les trois variables $dc, $domain, $dico sont bien définis avant de lancer le test.
  
  
### Cloud

- OVH

	- WordPress 

		- https://www.valdereuil.fr

- Server MS-OFFICE365

	- Business Plan1

	- Business Basic

	- Business Standard

### Applications

- TeamNet : AxelNet

- Horoquartz: E-temptation

- TeamNet: MobiliEcole

### Instant Access Point

- Administrateur

	- LAN

- Invité

	- Lan + Wan

- Hybride

	- LAN CHOISI (Spécifié)

## Pool Ressources

### Services

### Référant

## WI-FI Public

### Société Wi connect

- Point de connection espace public

	- 16 points

