# SSH
__Définition:__   
Secure Shell, est un protocol cryptographique utilisé pour opérer des services réseau de manière sécuriée.

SSH fonctionne en mode client-serveur. Le serveur SSH écoute sur un port
spécifique, généralement le port 22, pour les connexions entrantes.   

Une fois la connexion établie, l'authentification est réalisée, soit par mot de passe, soit par clés
publiques/privées. Après une authentification réussie, un shell sécurisé ou une session
de commande est établie, permettant l'exécution de commandes à distance.  
---
➔ Quels sont les protocoles qui ont été remplacés par SSH ?    

SSH a été créé pour remplacer les protocoles shell distants non sécurisés, 
tels que :
* Telnet *
* FTP 
* rsh 
* rlogin, 
* rexec.   
=>Ces protocoles sont par nature non sécurisés, lorsqu'ils échangent des informations, 
y compris les mots de passe en texte clair, ce qui nuit à la sécurité.  
---
➔ Quelles sont les différents modes d’utilisation de SSH (notamment au
  niveau de la sécurité)?  

 __Connexion SSH standard:__  
  Dans ce mode, SSH est utilisé pour établir une connexion sécurisée entre un client et un serveur. Les informations d'identification (nom d'utilisateur et mot de passe) ou une paire de clés SSH (clé publique/privée) sont utilisées pour authentifier le client.

  __Authentification par clé SSH :__  
  L'authentification par clé SSH est l'une des méthodes les plus sécurisées pour se connecter à un serveur SSH. Elle repose sur l'utilisation d'une paire de clés SSH, comprenant une clé privée (stockée sur le client) et une clé publique (stockée sur le serveur). L'accès est autorisé uniquement si la clé publique correspond à la clé privée.

  __Authentification à deux facteurs (2FA) :__  
  Pour renforcer la sécurité, SSH peut être configuré pour utiliser l'authentification à deux facteurs. Cela exige à la fois une clé SSH et un deuxième facteur d'authentification, tel qu'un mot de passe à usage unique (OTP) généré par une application mobile ou un jeton matériel.

  __Utilisation de certificats SSH :__  
  Les certificats SSH permettent une gestion centralisée des clés SSH et une autorisation granulaire. Les certificats SSH sont émis par une autorité de certification SSH et peuvent être configurés pour expirer, ce qui renforce la sécurité.

  __Port forwarding (tunneling) :__  
  SSH permet la création de tunnels sécurisés pour transférer des données sensibles à travers des réseaux non sécurisés. Cette fonctionnalité est souvent utilisée pour sécuriser l'accès à des services internes tels que les bases de données.

  __Désactivation de l'authentification par mot de passe :__  
  Pour améliorer la sécurité, vous pouvez désactiver complètement l'authentification par mot de passe et n'autoriser que l'authentification par clé SSH ou d'autres méthodes plus sécurisées.

  __Configuration de règles d'accès (ACL) :__  
  Vous pouvez configurer des règles d'accès pour contrôler qui est autorisé à se connecter au serveur SSH. Cela permet de restreindre l'accès en fonction de l'adresse IP, du groupe d'utilisateurs, etc.

  __Surveillance et journaux :__  
  Il est essentiel de mettre en place une surveillance et une journalisation appropriées pour détecter les activités suspectes et analyser les journaux d'authentification SSH.

  __Mises à jour régulières :__  
  Assurez-vous de maintenir votre serveur SSH à jour avec les dernières mises à jour de sécurité pour corriger les vulnérabilités connues.
  ---

➔ Comment est établie une connection SSH entre un client et un serveur avec
la méthode la plus sécurisé (faites un schéma)?  
 
![Schéma de connexion SSH sécurisée](ssh-linux-23)




| Catégorie                                         | ligne de Commande     |
|:--------------------------------------------------|:----------------------|
| Navigation et gestion de Fichiers                 | ls                    |
| entrer dans un dossier                            | cd                    |
| avoir la position actuelle                        | pwd                   |
| Manipulation de Fichiers et de répertoires        | cp                    |
| créer un répertoire                               | mkdir                 |
| créer, changer et modifier timestamps d'un fichier | touch                 |
|déplacer un fichier/ répertoire|mv|
|affichage et lecture de contenu de fichier|cat|
|visualiser un ficher sans le modifier|less|
|trouver un ficher/répertoire|find|
| recherche le modèle spécifié par le paramètre Modèle et écrit chaque ligne correspondant à la sortie standard|
|Transfert et Synchronisation de Fichiers|scp|
|Éditeur de Texte|vim|
|stransférer et de synchroniser des fichiers ou des répertoires entre une machine locale, un autre hôte, un shell distant, ou toute autre correspondance de ceux-ci.|rsync|
|créer, changer et modifier un fichier|nano|



# Mise en production d’applications sans conteneurisation

__PHP-FPM :__   
FastCGI Process Manager: est une interface SAPI permettant la communication entre un serveur Web et PHP, basée sur le protocole FastCGI.  
__Nginx :__  
est un logiciel de serveur web qui permet de donner à son utilisateur la possibilité de créer un serveur web très performant et fiable. 