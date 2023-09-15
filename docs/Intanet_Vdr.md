# Intranet_Vdr
cdc_mairie_val_de_reuil

## Table des matières

-  Présentation de la ville et du contexte général
-  Besoins Fonctionnels
-  Attendues en Accompagnement de projet
-  Obligation du candidat


### Présentation : contexte général de l'existant.
La ville de Val-de-Reuil souhaites mettre en place un intranet destiné aux employés de la mairie. En interne un besoin de communication pour une meilleur harmonie entre les différents services. Il existe déjà un système de formulaires,créer sur le site web de la ville hébergé chez le fournisseur OVH. Au sein du site web officiel il existe des pages privées, permettant aux services de gérer les différentes communication entre elles. Le but du futur intranet est d'apporter une plateforme sur laquelle tous les services puissent communiquer, partager, effectuer des reunions d'équipes, chat interne par groupe de travail.
De l'infrastructure actuelle une question cruciale se posait celle de la gestion des règles et permissions déjà présente sur l'Active Directorie. 

### Esxi Hypervisor : VDR_Lab Configuration 21-07-2023

#### VMware vSphere :  Hypervisor 8

Sauvegarde faite sur la machine distante disponible dans le dossier : C:\outils \chercher licence `VMware vSphere Hypervisor (ESXi ISO) image 2023-06-01 8.0U1a 599.47 MB iso`

> !!! tip  "Vmware notes"

      Boot your server with this image in order to install or upgrade to ESXi (ESXi requires 64-bit capable servers). This ESXi image includes VMware Tools.
      md5sum(¹): 05768de15c1cf8790af9702c077493e5
      sha1sum(¹): ce142434b34c994c9712651eac35099db973bd76
      sha256sum(¹): fe1ba819ce9a84318a4cf39ca0bd273009089f5abf86c49b002f46b05d399514

#### ISO : Vmware

1. Voir le fichier word pour la config préalable de VmWare workstation.
2. Configurer le réseau interne : il est recommander de sélectionner deux réseaux lors de la configuration afin de pourvoir plus tard réaliser les actions tel que créer un cluster.
3. VLAN : optionnel configuration si nous allons utiliser une segmentation de notre réseau plus tard.

!!! info "Ma dernière config"
      Ma dernière configuration est à reprendre entièrement
      je vais charger l'image car j'ai crée un compte avec une licence se référer à la clé
      cmd utiles pour la gestion des patch : exicli software update -d.

    Bibliothèque vmware_profile
      [vmware doc installation](https://docs.vmware.com/fr/VMware-vSphere/8.0/vsphere-esxi-installation/GUID-B2F01BF5-078A-4C7E-B505-5DFFED0B8C38.html)
      [document complémentaire](https://www.vmware.com/techpapers.html)

!!! important "Bibiothèque partagé"
     [Lien de lecture](https://docs.vmware.com/)


### Ma configuration VMware_Workstation

#### Esxi 1 :

1. Mémoire : 24.3 GB soit 24836
2. Processeurs : Nombre de 3 et 1 pour le nombre de cœur par processeur
3. Disques durs :
   1. 32 GB
   2. 3.2 64 GB
      Le tout en dynamique.
4. Configuration Réseau : Bridged (Automatic) connecté directement au réseau physique

#### Esxi 2 :

1. Mémoire : 21.1 GB soit 21620
2. Processeurs : Nombre de 3 et 1 pour le nombre de cœur par processeur
3. Disques durs (SCSI):
   1. 3.1 32 GB
   2. 3.2 70 GB
      Le tout en dynamique.
4. Configuration Réseau : Bridged (Automatic) connecté directement au réseau physique
5. Configuration réseau 2 : Host-only

!!! Important "BIOS CONFIGURATION Virtualization Support"
     Sous Windows il faudrait activer l'hote de confiance dans la virtualisation sous vmware pour arriver à émuler nos esxi, et vcenter.Sans cela il y'aura un bug
      >> [!bugs] Bugs config
      >> Enable VT for Direct I/O
      >> Pour rappel : nous sommes sous une machine Dell technologie Intel, Windows 10.


## Benchmarking Propositions : Mattermost, Wordpress, Etherpadlite

En ayant configuré un environnement de test personnalisé , j'ai pu testé la solution avec Wordpress. Certe il vrai qu'il existe des solutions permettant d'intégré Light (LDAP) via plusieurs pluggins. Il n'en reste pas moins que la solution finale pour un accès interne sera de déployer le site sous le fournisseur OVH. Une sorte de duplicata du site actuelle uniquement accessible que par les employés de la ville. Durant mes recherche pour une solution interne, à moindre coût, secure et parfaitement opérationnel, il y'a la solution Mattermost. J'ai testé la solution Etherpad lite, elle est à priori intéressante car on peut y rajouter des fonctionnalités supplémentaire depuis le market-place. Il reste restreint à une petite équipe et focus sur le partage de fichier collabortif en temps réel, un éditeur en temps réel avec possibilité de tchat intégré.
J'ai donc installé et testé la solution proposé par Mattermost. Il regroupe les fonctionnalités de tchat, comme microsoft teams, le partage de documents presque tout format supporté (gif, word, excel, ppt, etc).

|Nom |Statut | coûts | avantages | inconvenients |lien |
|:---|:-------|:-----|:----------|:--------------|:-----|
|Sharepoint| Propriétaire |Licence Office365| existantes| coût/par Personne|[Microsoft sharepoint](https://www.microsoft.com/fr-fr/microsoft-365/sharepoint/collaboration)|
|Nexcloud| libre | Solution Entreprise | Herbergements onprem ou fournisseurs| maintenabilité (personne dédié)|[NextCloud](https://nextcloud.com/fr/install)|
|EherpadLite| OpenSource| gratuit|totalement gratuit| mise en place et maintenance|[etherpadLite](https://github.com/ether/etherpad-lite)|
|Mattermost | Libre| gratuit-payant| auto-hébergé: chat interne, partage de documents|version payante 10$/mois| [mattermost](https://mattermost.com)|




### Présentation : Mattermost Val-de-Reuil
- Fedora Iso
- Workstation vmware
- Docker
- Mobaxterm

#### Jonction à l'infra
La solution proposée devra pour être intégré à l'infrastruce existante respectée les normes de sécurité du site. Il faudrait pour cela qu'il soit hébergé en locale. J'ai opté pour une distribution Linux Fedora server (RedHat) version 38, la plus récente au moment où j'écris ces notes. 

#### Environnement : virtuel
Dans l'optique où je n'ai pas d'accès au réseau en locale. j'ai émulé une solution possible sur vmware-workstation.
Il faudrait donc pour être dans les mêmes conditions disposer d'une version 16^. Charger une image iso téléchargeable [ici, fedora-serveur](https://fedoraproject.org/server/).
J'ai opté pour une solution embarqué sous docker, lors de  l'installation du service Mattermost, pour des raisons simples de gestion, mise à jour et maintenabilité. Mais aussi la possibilité de le déployer sous un serveur windows si besoin.

#### Install et configuration sous docker
Pour le contrôle et la prise à main à distance j'utilise [Dwsservice.net](https://www.dwservice.net/). Si docker n'est pas installer il faudrait le faire.
- Procédure d'installation et configuration.
Une fois votre serveur en route, configuré pour une connection ssh, se rendre sur mobaxterm et lancer les commandes suivantes.
```bash
dnf update --refresh -y 
# fedora possède son propre gestionnaire docker
dnf install moby-engine
# démarrer le systeme 
systemctl start docker
# rendre globale docker, pour l'utiliser sans 'sudo'
usermod -aG docker root
# lancer la preview de mattermost
docker run --name mattermost-preview -d --publish 8065:8065 mattermost/mattermost-preview
docker start mattermost-preview
# gérer le parefeu
firewallcmd --zone=public --add-port=8065/tcp --permanent
firewallcmd --reload
# redemarrer pour une prise en compte des modifications 
shutdown now -r
# !!!!!!!Attention: ne pas oublier de redemarrer les services docker!!!!!!!!
```
Les services ont bien démarré, nous pouvons nous rendre dans notre navigateur et procéder à la configuration des différents espaces de communication.
Tout d'abord je vais créer un administrateur locale.

```html
<div class="tooltip" id="n0">PC</div>
<div class="tooltip" id="n1">PC_5</div>
<div class="tooltip" id="n2">192.168.xx.xx</div>
<div class="tooltip" id="n3">192.168.xx.xx</div>
<div class="tooltip" id="n4">192.168.xx.xx</div>
<div class="tooltip" id="n5">192.168.xx.xx</div>
<div class="tooltip" id="n6">## Confiuration de Vsphere <br>Ip addresse : 1xx.xxx.xx.xxx<br>domain : lab4valdereuil.local <br>Single Sign On : administrator@lab4valdereuil.local<br>Password : Pa$$w0rd<br>## Cluster de Haute Disponibilité : labvaldereuil_clusterHa<br>statut : sain<br>Serveur Active Directory  état sain <br><br>page d'administration web<br><br>Durée de la licence restante à la date du 26/07/2023, 59 jours.<br></div>
<div class="tooltip" id="n7">Domaine : lab4valdereuil.loc
  <br>ip address AD : 192.xxx.xx.xxx
  <br>DNS :
  <br>!Important : voir le script disponible pour la création en powershell
  <br>## srv-ad1 configuration :
  <br>script : 
  <br>ipconfig /all
  <br>rename-computer -newname SRV-AD1
  <br>restart-computer
  <br>New-IPAddresses -IPAddresses 192.xxx.xx.xxx -PrefixLength 24 -DefaultGateway 192.xxx.xx.xxx -interfaceAlias Ethernet0
  <br># set timezone
  <br>Tsutil.exe /s "Romance Standard Time"
  <br>restart-computer
  <br># Install ADDS rôle 
  <br>Install-WindowsFeature AD-Domain-Services - includeAllSubFeature -IncludeMangementTools  
  <br># Import des module ADDS optionnel
  <br>Import-Module ADDSDeployment
  <br># Install nouvelle forêt
  <br>Install-ADDSForest -CreateDnsDelegation:$false -DatabasePath "C:\Windows\NTDS" -DomainMode ""Win2012R2"" -DomainName "labvaldereuil.local" -DomainNetBiosName "LAB4VALDEREUIL" -ForestMode ""Win2012R2"" -InstallDns:$true -LogPath "C:\Windows\NTDS" -NoRebootOnCompletion:$false -SysvolPath "C:\Windows\SYSVOL" -Force:$true
  <br># Install DHCP et DNS services
  <br>set-DnsServerForwarder -IPAddress 4.2.2.1 -ComputerName SRV-AD1
  <br>Install-WindowsFeature -computername SRV-AD1 -Name DHCP -IncludeManagementTools
  <br># complete configuration du dhcp 
  <br>netsh dhcp add securitygroups
  <br># ajouter le server à l'Active Directory
  <br>Add-DhcpServerInDC -IPAddress 192.xxx.xx.1 -DnsName srv-ad1.labvaldereuil.local 
  <br>#Creation du scope initial des plages d'addresses pour le réseau 192.xxx.xx.0
  <br>Add-DhcpServerv4Scope -Name 'lab users scope" -ComputerName srv-ad1 -StartRange 192.xxx.xx.xx -EndRange 192.xxx.xxx.xxx -SubnetMask 255.255.255.0 -LeaseDuration 8.00:00:00
  <br># creation des valeurs optionnel pour le serveur DHCP 
  <br>set-DhcpServerv4OptionValue -ScopeId 192.168.10.0 -ComputerName srv-ad1 -DnsDomain lab4valdereuil.local -router 192.xxx.xx.1 -DnsServer 127.0.0.1 
  <br>!!!IMPORTANT Notes: ici je suis en local sur le réseau host-only.
  <br></div>
<div class="tooltip" id="n8">vmare workstation last edition 17.0.2<br>winget search vmare
   <br>winget install  VMware.WorkstationPlayer
   <br><br>iso : windows server 2019<br></div>
<div class="tooltip" id="n9">srv_mattermost<br>
  <br>federo server
  <br>2go ram
  <br>1Vcpu
  <br>20go de disk
  <br>---
  <br>docker image : matterost-mattermost-preview
  <br>---
  <br></div>
```

## Additionnel : AgoraProject 
Voici les incontournables dans le besoin exprimé, l'intranet devra avoir les fonctionnalités suivantes : 
- Gestion de l'agenda des manifestations de la ville
- Agenda des réunions publiques des élus
- Programmation des réunions (CTM,CCAS, Hôtel de ville)
- Base documentaire : organisation générale, notes de services rapports d'activités, plan des bâtiments 
- Ressources Humaines: Fiche de poste, Bourse à l'emploi mouvements : "onbording"
- Marché publics : modèles de documents , marchés en cours et projet
- Trombinoscope et annuaires : Annuaire/organigramme interne, annuaires des élus, annuaires externes
- Finances : Préparation budgétaire, documents budgétaires, subventions
- Conseil Municipal : Délibération, comptes rendus, composition des instances 
- Dispositif d'astreinte de gestion des crises : guide des procédures d'astreinte, plan commmunal de sauvegarde
- Informations externes : Abonnement presse, revues sites externes conseillés.
- Applications téléprocédures et outils de travail : accès aux applications internes

### Préconisations : Omnispace developpé par AgoraProject 
[site web](https://agora-project.net/)

Agora project est open source fait en France, susceptible de répondre à l'ensemble des besoins formulés. le guide d'utilisateur est très bien écrit et sa prise en main ne nécessite pas de grandes compétences en informatique. 
Il existe deux manières de l'utiliser : 
1. En souscrivant à une offre Omnispace 
2. En [auto-hébergeant agora-Project](https://github.com/xech/agora-project)

