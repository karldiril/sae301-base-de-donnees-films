# Livrable 4 : Présentation du projet 



## 1 - But et public visé

L'objectif de ce projet est de réaliser une application qui utilisera des informations brutes issues d’une base de données ou calculées grâce à des algorithmes à partir de données dans le but de présenter des informations à la communauté d'utilisateurs telle que des films afin de pouvoir consulter leurs fiches, c’est-à-dire permettre à l'utilisateur du site de rechercher des films ou séries de films via des mots-clés pour afficher la fiche associée au film et naviguer d’une fiche à une autre. Le public visé par ce projet est assez large, il s’étend de l’amateur cherchant des informations sur un film, une série de films, un réalisateur en particulier, mais il peut également s’étendre à des personnes passionnées de cinéma à la recherche de nouveautés, comme aux professionnels du milieu en quête d’informations concrètes sur un genre de film par exemple. Le public visé est donc large, le projet doit donc permettre d'être accessible au plus de personnes possible.



## 2 - Particularités du projet

Ce projet possède de nombreuses particularités, il doit exploiter et utiliser des données brutes issues du site “IMDb”. Ces données ne contiennent pas seulement des films mais aussi des séries avec des épisodes. Ces données seront sous forme de fiches qui contiendront plein d’informations telles que le titre, la durée, le réalisateur, l'année de sortie, les acteurs qui y ont joué. Par ce fait, ce projet doit permettre de naviguer de fiche en fiche en passant par les acteurs qui permettront donc de passer d’un film à un autre en passant par un acteur/actrice qui a joué dans ce film grâce à un système de rapprochement de films, et le site doit permettre, après avoir sélectionné deux films ou deux acteurs, les personnes ou les films qu’ils ont en commun. Également, ce projet doit intégrer une barre de recherche qui permet de rechercher une personne par son nom ou prénom et un film par son titre. Cette barre de recherche doit également pouvoir proposer une recherche avancée qui permet de sélectionner par d’autres critères, une personne ou un film avec une ressemblance approximative et aussi une sélection par tri (ex. : date, ordre alphabétique, etc.).

Ce projet intègre trois grands algorithmes : plus courte chaîne dans un graphe biparti.

- Le premier aura pour but de réaliser une recherche approximative grâce à une plage de temps, par exemple avec des naissances, ou avec la création de films pour afficher tous les films du même réalisateur que le film recherché.
- Le second devra permettre de faire des recherches sur les éléments en commun dans des films différents avec, par exemple, des duos d'acteurs.
- Le troisième permettra de créer des liens entre les acteurs et les films dans le but de passer d'un acteur à un film dans lequel il a joué, puis à un autre acteur et ainsi de suite.

Elle utilisera plusieurs sources telles que POSTGRESQL, APACHE, Grafana, JavaScript, PHP, SQL, Bootstrap.



## 3 - Sécurité

La sécurité est aussi une grande partie du projet car elle vise à garantir la confidentialité, l'intégrité, la disponibilité et la traçabilité au minimum. Pour ce faire, nous devrons réaliser une séparation des différents rôles pour qu’un rôle ne puisse faire uniquement ce dont il a besoin. Nous devrons également faire attention aux données extérieures en ne leur accordant aucune confiance. Nous devons par ailleurs lutter contre les injections SQL, créer des sauvegardes régulières de la base de données et les tester, chiffrer ou hacher les données sensibles et limiter la quantité de données collectées. La création de cookies pour la connexion, la déconnexion et l'expiration sont à prévoir, mais aussi vérifier les droits côté serveur, les injections HTML, les attaques CSRF, les validations d'entrée, la gestion des erreurs et les en-têtes HTML. La sécurité de notre site va beaucoup être centrée sur les permissions des différents rôles et les injections SQL, HTML, ... 
