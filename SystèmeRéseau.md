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
  

---

# Mise en production d’applications sans conteneurisation

__PHP-FPM :__   
FastCGI Process Manager: est une interface SAPI permettant 
la communication entre un serveur Web et PHP, basée sur le protocole FastCGI.  
__Nginx :__  
est un logiciel de serveur web qui permet de donner à son 
utilisateur la possibilité de créer un serveur web très performant et fiable.   

--- 
➔ Quelles sont les problématiques qui vont survenir par rapport à la gestion
des différents code source (notamment par rapport à la diversité des
technologies)?  
1- Complexité de la gestion : Plusieurs projets signifient plus de fichiers, de dossiers et de configurations à gérer. Cela peut devenir rapidement complexe, en particulier si les projets ont des structures de dossiers différentes ou des normes de nommage variées.

2- Diversité des langages et des frameworks : Chaque projet peut utiliser un langage de programmation différent (par exemple, Python, JavaScript, PHP, Java, etc.) avec ses propres frameworks et bibliothèques. Cela peut rendre difficile la maintenance et la mise à jour des différentes technologies.

3- Versions de logiciels : Les projets peuvent nécessiter différentes versions de logiciels, de bibliothèques et de dépendances. Il peut être difficile de gérer ces dépendances et de s'assurer qu'elles ne sont pas en conflit les unes avec les autres.

4- Cycle de vie des applications : Les projets peuvent avoir des cycles de vie différents. Certains peuvent être en développement actif, tandis que d'autres sont en maintenance ou en phase de support. Il est important de gérer ces différences pour allouer des ressources de manière appropriée.

5- Intégration continue et déploiement continu (CI/CD) : L'automatisation des tests, de la construction et du déploiement peut devenir complexe lorsque plusieurs projets sont impliqués, en particulier s'ils utilisent des outils et des pipelines différents.

6- Collaboration d'équipes : Si plusieurs équipes travaillent sur différents projets, la collaboration et la coordination peuvent devenir un défi. La communication et la synchronisation entre les équipes deviennent cruciales.

7- Gestion des erreurs et débogage : Le débogage et la gestion des erreurs deviennent plus complexes lorsque plusieurs technologies sont impliquées, car chaque technologie peut avoir ses propres outils et méthodes de débogage.

8- Sécurité : La sécurité doit être prise en compte pour chaque technologie utilisée, car les failles de sécurité peuvent varier d'une technologie à l'autre. Une mise à jour de sécurité dans l'une des technologies peut nécessiter une action immédiate.

9- Documentation : La documentation est essentielle pour comprendre chaque projet et ses spécificités. Assurez-vous que chaque projet est correctement documenté pour faciliter la maintenance et la résolution de problèmes.

10-  Évolutivité : Les besoins de chaque projet peuvent évoluer avec le temps. Vous devrez être prêt à adapter les technologies, les architectures et les ressources en fonction de ces besoins changeants.  
  
---
La conteneurisation est une technologie qui offre de nombreux avantages en matière de développement, de déploiement et de gestion d'applications. Voici quelques-uns des avantages les plus importants de la conteneurisation, expliqués en termes simples :  
1- Portabilité : Les conteneurs encapsulent une application et toutes ses dépendances (bibliothèques, fichiers système, etc.) dans un seul package. Cela signifie que vous pouvez exécuter le même conteneur sur n'importe quel environnement compatible, que ce soit un ordinateur portable de développement, un serveur de production ou même un cloud public. Cette portabilité facilite le déploiement d'applications cohérentes sur différentes infrastructures.

2- Isolation : Chaque conteneur fonctionne dans un environnement isolé par rapport aux autres conteneurs et au système hôte. Cela garantit que les applications ne se gênent pas mutuellement ni n'entrent en conflit avec les dépendances système. L'isolation renforce également la sécurité en limitant l'accès des conteneurs aux ressources du système.

3- Légèreté : Les conteneurs sont plus légers que les machines virtuelles (VM). Ils partagent le même noyau du système d'exploitation avec le système hôte, ce qui réduit la surcharge de ressources. Cela signifie que vous pouvez exécuter davantage de conteneurs sur un serveur donné, ce qui économise des ressources et réduit les coûts d'infrastructure.

4- Facilité de déploiement : La création, la distribution et le déploiement de conteneurs sont automatisés à l'aide de fichiers de configuration (généralement des fichiers Dockerfile). Cela facilite grandement le processus de déploiement, de mise à jour et de mise à l'échelle des applications, ce qui permet de gagner du temps et d'éviter les erreurs humaines.

5- Gestion des versions : Les conteneurs permettent de gérer les versions des applications de manière efficace. Chaque version de l'application peut être encapsulée dans un conteneur distinct, ce qui facilite la gestion des mises à jour et des rétrocompatibilités.

6- Microservices : La conteneurisation s'intègre bien avec l'architecture des microservices, où une application est décomposée en petits services indépendants. Chaque service peut être mis en conteneur, ce qui facilite le déploiement, la mise à l'échelle et la gestion individuelle des services.

7- Évolutivité : La mise à l'échelle des applications conteneurisées est plus simple. Vous pouvez facilement ajouter ou retirer des conteneurs pour gérer la charge de travail en fonction des besoins. Les orchestrateurs de conteneurs, tels que Kubernetes, simplifient la gestion de l'évolutivité automatique.

8- Développement plus rapide : Les conteneurs permettent aux développeurs de travailler dans des environnements de développement cohérents avec la production. Cela réduit les problèmes de "ça fonctionne sur ma machine" et accélère le cycle de développement.

9- Sécurité : Bien que la sécurité dépende de la configuration appropriée des conteneurs, l'isolation inhérente et les mécanismes de contrôle d'accès renforcent la sécurité par rapport à l'exécution d'applications directement sur le système hôte.  
  
---  
# Mise en production d’applications

Docker repose sur plusieurs concepts clés qui permettent de comprendre son
fonctionnement et son utilité. Voici les concepts de base associés à Docker :  
● Image : Une image Docker est un modèle immuable utilisé pour créer un
conteneur. Elle contient le code source de l'application, les bibliothèques, les
dépendances et autres fichiers nécessaires à l'exécution de l'application.  
● Dockerfile : C'est un fichier de script qui contient les instructions pour
construire une image Docker.  
● Conteneur : Un conteneur est une instance exécutable d'une image Docker. Il
s'agit d'une encapsulation légère d'une application et de son environnement
d'exécution, fonctionnant de manière isolée sur le système hôte.  
● Registry : Zone de stockage pour les images Docker. Il peut être public ou privé
(pour une utilisation interne en entreprise par exemple). Docker Hub est un
service cloud public pour partager et stocker des images Docker. C'est comme
un "GitHub" pour les images Docker, où les développeurs peuvent push ou pull
des images.  
● Volume : Les volumes sont utilisés pour persister les données et partager des
fichiers entre le conteneur et l'hôte. Ils sont essentiels pour éviter la perte de
données lorsque les conteneurs sont arrêtés ou supprimés.  
● Réseau Docker : Docker possède sa propre gestion du réseau, permettant aux
conteneurs de communiquer entre eux et avec des ressources extérieures. Il
offre plusieurs modes réseau comme "bridge","host" et"overlay"  
● Docker Compose : C'est un outil pour définir et gérer des applications
multi-conteneurs. Avec Docker Compose, on peut définir une application à
l'aide de plusieurs conteneurs dans un seul fichier, puis démarrer ces conteneurs
simultanément avec une seule commande. Par exemple, vous voulez déployer
une application PHP qui utilise une base de données MySQL. Vous allez écrire
un fichier docker-compose qui va décrire la configuration du conteneur pour
PHP et le conteneur MySQL. Cela va éviter de lancer les commandes à la main
et permettre d’avoir un suivi dans Git.

➔ Que fait Docker si l'image demandée n'est pas présente localement?  
Lorsque vous demandez à Docker de lancer un conteneur à partir d'une image qui n'est pas présente localement sur votre système, Docker va automatiquement chercher cette image dans un registre d'images Docker, généralement le registre par défaut est Docker Hub, mais vous pouvez également spécifier d'autres registres.

Voici ce qui se passe lorsque vous demandez à Docker de lancer un conteneur avec une image qui n'est pas présente localement :

* Docker recherche l'image localement : Tout d'abord, Docker vérifie si l'image que vous avez spécifiée existe déjà localement sur votre système. Si l'image est déjà téléchargée et présente localement, Docker utilisera cette image pour créer le conteneur.

* Docker recherche dans les registres : Si Docker ne trouve pas l'image localement, il effectuera une recherche dans les registres d'images Docker spécifiés (par défaut, Docker Hub). Il tentera de télécharger l'image depuis le registre correspondant.

* Téléchargement de l'image : Si l'image est trouvée dans le registre, Docker la téléchargera sur votre système. Le processus de téléchargement dépend de la taille de l'image et de la vitesse de votre connexion Internet. Une fois le téléchargement terminé, l'image sera stockée localement sur votre système pour une utilisation ultérieure.

* Création du conteneur : Après avoir téléchargé l'image, Docker utilisera cette image pour créer un conteneur en fonction des paramètres que vous avez spécifiés, tels que les options de ligne de commande, les ports exposés, les volumes montés, etc.

* Démarrage du conteneur : Une fois le conteneur créé, Docker le démarre, et il sera opérationnel et exécutera les processus définis dans l'image.