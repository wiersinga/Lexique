
# Application à Page Unique (SPA)

Une application à page unique est une application qui interagit avec les utilisateurs en réécrivant les pages Web existantes avec de nouvelles données provenant du serveur Web, au lieu d’utiliser la technique par défaut du navigateur qui exécute une toute nouvelle page.

L'objectif est d'avoir des transitions plus rapides qui peuvent faire en sorte que le site se sente plus comme une application inhérente.

Dans un SPA, tout le code HTML, JavaScript et CSS requis est soit récupéré par le navigateur, soit des ressources appropriées qui sont chargées et ajoutées aux pages selon les besoins.  Cela se produit généralement en réponse aux actions de l'utilisateur.

La page ne se recharge à aucun moment de la procédure et ne transfère pas le contrôle à une autre page, bien que l'API historique HTML5 ou le hachage de l'emplacement puissent être utilisés pour offrir la navigabilité et la perception de pages logiques distinctes dans l'application Web.

## Comment fonctionne une SPA ?

### MPA (Multiple Page Application) - concept de base

SPA et MPA sont tous deux basés sur le protocole HTTP.

Dans une architecture MPA client/serveur traditionnelle, chaque clic de l'utilisateur déclenche une requête HTTP vers le serveur. Le résultat de cette nouvelle requête est un rafraîchissement complet de la page, même si une partie du contenu reste inchangée.

### SPA - Ajax et JavaScripts

Le cœur d'un SPA est basé sur Ajax, un ensemble de techniques de développement qui permet au client d'envoyer et de récupérer des données du serveur de manière asynchrone (en arrière-plan) sans interférer avec l'affichage et le comportement de la page web. Ajax permet aux pages web et, par extension, aux applications web, de modifier le contenu de manière dynamique sans avoir à recharger la page entière.

Pour ce faire, les SPA s'appuient fortement sur des scripts Java qui s'exécutent dans le navigateur du client. Les frameworks JavaScript tels que React, Vue, Angular et Ember sont chargés de s'occuper du gros travail côté client.

En résumé, un SPA fonctionne comme suit :

- Le client se connecte d'abord au serveur et obtient le contenu de la page, qui correspond principalement au code HTML, au CSS et à un bundle JavaScript, contenant tous les JavaScripts nécessaires pour exécuter la logique de l'application.
- L'action d'un utilisateur déclenche l'exécution de JavaScript associés, qui à leur tour demandent des données au serveur par le biais d'appels Ajax. Les données sont généralement fournies dans un format JSON et ne déclenchent pas de rafraîchissement complet de la page Web.

Dans une application multi-tiers (MPA) impliquant des serveurs back-end, le serveur web peut se contenter de télécharger le paquet initial de HTML/CSS/JavaScript. Tous les appels Ajax ultérieurs se font directement entre le navigateur et les services back-end.

## Quels sont les avantages d'une application à page unique (SPA) ?

Les applications à page unique sont connues pour tirer parti des mises en page répétitives et du contenu à la demande. Comme elles tirent parti de ces deux concepts, elles sont beaucoup plus efficaces, coûtent nettement moins cher que les applications traditionnelles et consomment également moins d'énergie. Voici quelques avantages à l'utilisation des applications à page unique.

### Vitesse accrue

La vitesse doit être l'un des plus grands avantages d'opter pour le développement d'une application à page unique. Elles sont beaucoup plus rapides que les applications web traditionnelles car elles peuvent charger de nouvelles informations dans une seule page à la demande du client au lieu de relier plusieurs pages HTML à l'architecture du site.

Comme l'application n'a pas besoin d'envoyer constamment des requêtes au serveur et d'attendre de télécharger une nouvelle page à partir de zéro, une application à page unique est beaucoup plus facile.

### Expérience utilisateur (UX)

Comme nous l'avons vu précédemment, les applications à page unique sont les leaders en matière d'expérience utilisateur pratique et directe. La plupart des utilisateurs sont souvent déroutés et irrités de devoir cliquer sur de nombreux liens dans une application traditionnelle pour arriver là où ils veulent.

Les applications à page unique éliminent ce problème en fournissant tout le contenu nécessaire dans une seule page déroulante. Cela fait également



**Un tableau comparatif des principaux frameworks** 

| Framework            | Date de Création | Communauté / Entreprise  | License       | Points Forts                                    | Points Faibles                                      |
|---------------------|------------------|---------------------------|---------------|-------------------------------------------------|-----------------------------------------------------|
| **Angular**         | 2010             | Google                   | MIT           | - Structure solide et complète                 | - Courbe d'apprentissage abrupte                    |
|                     |                  |                           |               | - Gestion des composants                       | - Complexité parfois excessive                     |
|                     |                  |                           |               | - Forte typage avec TypeScript                 |                                                     |
| **React**            | 2013             | Facebook                  | MIT           | - Vue dynamique et efficace                    | - Bibliothèque, pas un framework à part entière   |
|                     |                  |                           |               | - Composants réutilisables                     | - Besoin de bibliothèques tierces pour fonctionner  |
|                     |                  |                           |               | - Large communauté et écosystème               |                                                     |
| **Vue.js**           | 2014             | Evan You (Open Source)    | MIT           | - Facilité d'apprentissage                      | - Moins adapté aux applications complexes         |
|                     |                  |                           |               | - Vue déclarative                              |                                                     |
|                     |                  |                           |               | - Composants simples et réactifs               |                                                     |
| **Ember.js**         | 2011             | Ember.js Core Team        | MIT           | - Conventions fortes                            | - Courbe d'apprentissage abrupte                    |
|                     |                  |                           |               | - Structure de projet intégrée                 | - Lourdeur pour des projets simples                |
|                     |                  |                           |               | - Routing intégré                              |                                                     |
| **Meteor**           | 2012             | Meteor Development Group | MIT           | - Développement rapide d'applications web       | - Moins adapté aux applications non-SPA (Single Page Application)  |
|                     |                  |                           |               | - Partage de code sur le client et le serveur   | - Moins de flexibilité pour le back-end            |
|                     |                  |                           |               | - Live data updates                            |                                                     |
| **Ruby on Rails**    | 2005             | Basecamp (Open Source)    | MIT           | - Productivité élevée                           | - Meilleur adapté aux applications web traditionnelles  |
|                     |                  |                           |               | - Conventions de codage claires                 | - Performance peut être un problème pour certaines applications lourdes  |
|                     |                  |                           |               | - Génération de code automatique               |                                                     |
| **Django**           | 2005             | Django Software Foundation | BSD          | - Sécurité intégrée                            | - Surdimensionné pour les petites applications     |
|                     |                  |                           |               | - Rapidité de développement                    | - Courbe d'apprentissage pour les débutants        |
|                     |                  |                           |               | - Bonnes pratiques intégrées                   |                                                     |
