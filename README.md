# LifeBuilder



Ce site permet d'avoir un registre organisé de ses personnages personnel. 

Il permet de noter les informations de ses personnages que ce soit des idées simples et peu avancé ou l'équivalent d'une trilogie. 
On peut y créer une simple fiche de personnage avec des descriptions simple sous forme de texte et d'image (nom, âge, couleur de peau, de cheveux etc...) et y ajouter des informations plus détaillés ( backstory, hobbys, relations avec les autres personnages, évolution dans l'histoire).
Le but est d'avoir une création de personnage permettant des descriptions très courtes et simples mais aussi des plus complexes et développées.

Les utilisateurs pourront aussi utiliser des catégories (tels que l'univers du personnage ou une particularité commune à plusieurs personnages) et tags (des caractéristiques trop communes ou plus simples) de leurs choix pour leurs personnages et les retrouvés plus simplement sur leurs profils.

Enfin, les utilisateurs pourront rendre leurs personnages publics et les partager et commenter sur les pages des autres utilisateurs.  

=====================================================================================================================================

Versions du projet
Php: 8.4
Symfony 7.3
Composer: 2.9.3
PostgreSQL: 16
Des versions égales ou supérieurs seront donc necessaires pour le bon fonctionnement du projet

========================================================================================================================================

Commandes utiles:

Pour le moment, le site n'est accessible qu'en local. Pour le voir:
- Cloner le projet
- Installer les dependances necessaires (verifier vos versions et n'oubliez pas le composer install)
- Liez votre base de donnée dans un .env.local (DATABASE_URL="postgresql://app:!ChangeMe!@127.0.0.1:5432/app?serverVersion=16&charset=utf8")
- Faites php bin/console doctrine:database:create
- Aller sur le dossier life-builder
- Faites la commande :symfony server:start.

php bin/console app:clean-sanctions 
Regarde quelles sanctions sont encore en cours et celles dont la date et dépassé. Si la date est dépassé, la sanction est enlevé et le modstatus repasse en "Pas de sanction".
/!\ Le lancement manuel de cette commande est temporaire, sur un serveur, cette commande devra être lancé tous les jours à X heure.

Diagramme UML: https://www.figma.com/board/3DCMfzPHGoC6asbxm1AFMN/UMLLifeBuilder?node-id=0-1&t=YzoSViaSo6XZLThc-1
Maquette : https://www.figma.com/design/uBSlsWzSc8Qlvsi7lyFAg0/LifeBuilder?node-id=0-1&t=TDX8wmZq05W0SriS-1
