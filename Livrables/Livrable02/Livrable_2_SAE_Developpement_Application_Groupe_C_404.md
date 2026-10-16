# Livrable 2 : Analyse des conditions juridiques 

Pour que notre logiciel soit conforme sur le plan contractuel et légal, notre projet doit respecter simultanément deux sources juridiques complémentaires d’IMDb :
Les conditions générales d’utilisation du service ([copyright/license](https://www.imdb.com/conditions?ref_=helpms_ih_gi_usedata)), qui définissent le droit d’auteur et l’accès au site, ainsi que les clauses de la license non commerciale ([Non-Commercial Licensing](https://help.imdb.com/article/imdb/general-information/can-i-use-imdb-data-in-my-software/G5JTRESSHJBBHTGX?pf_rd_m=A2FGELUUNOQJNL&pf_rd_p=1ed1aea6-d2ad-4705-95fd-ba13f1b5014f&pf_rd_r=XRE3QWF2G5YWTD2SGT0V&pf_rd_s=center-1&pf_rd_t=60601&pf_rd_i=interfaces&ref_=fea_mn_lk1#)) qui encadrent l’usage des fichiers de données mis à disposition par IMDb.  



  
## 1. Ce que nous avons le droit de faire 

IMDb nous accorde une licence gratuite, non exclusive et non transférable pour télécharger et stocker des copies locales de ces données sur nos machines (Condition of Use section “License And Site Access” des conditions d’utilisation et règle 3 de l’article d’aide “Can I use IMDb data in my software?”). Notre application s’inscrit dans ce cadre, il s’agit bien d’un projet étudiant sans but lucratif, ce qui respecte les attentes.

Cependant, cette même règle 3 précise que les données ne peuvent pas être modifiées, publiées, revendues ou réutilisées afin de créer une base de données à laquelle on peut accéder en ligne ou hors ligne. Cette contrainte implique que notre application ne peut pas être mise en ligne en accès public sur Internet. Le déploiement doit donc rester dans un environnement privé. 


## 2. Contraintes techniques imposées au développement

Les documents imposent trois obligations pour la réalisation côté technique : 

Nous ne pouvons pas republier ou redistribuer les données brutes (règle 3 de la page d’aide “Can I use IMDb data in my software?”). Cela veut donc dire que nous ne pouvons pas versionner les jeux de données sur notre dépôt partagé Github. Ainsi le dépôt ne doit contenir que le code source, les fichiers de récupération et les schémas relationnels. Pour ce qui est des données, nous les importerons via un script shell qui télécharge les archives à la bonne adresse pour répondre aussi aux attentes du livrable 5.

Deuxièmement, la méthode de récupération des données est encadrée.
La règle 2 du même article interdit l’utilisation de techniques d’extraction automatisée telles que le web scraping, les robots ou le data mining directement sur le site d’IMDb, sauf autorisation écrite. Nous devrons donc récupérer les données à partir des fichiers officiels fournis par IMDb, notamment au format TSV (https://datasets.imdbws.com).


La règle 4 de cette même page impose d’afficher de façon visible sur l’interface de notre site la mention exacte rédigée par IMDb : 

“Information courtesy of IMDb (https://www.imdb.com)
Used with permission. ”


## 3. Garanties et responsabilités

Dans la section “Disclaimer of Warranties and Limitation of Liability” de ses Conditions d’utilisation ([copyright/license](https://www.imdb.com/conditions?ref_=helpms_ih_gi_usedata)), IMDb indique que les données sont fournis en l’état et selon disponibilité, sans garantie d’exactitude, de mise à jour ou de continuité de leur service, cela implique que les données risquent d’être moins pertinentes que celles présentes sur leur site web. De plus, la règle 1 de la page d’aide informe qu’IMDb se réserve le droit de retirer l’autorisation d’utiliser les données à tout moment et sans préavis.


## 4. Droits à négocier en cas d’exploitation commerciale

Dans le cas où notre plateforme deviendrait un produit commercial ouvert au public (avec des fonctionnalités payantes ou de la publicité), les jeux de données utilisés ne seraient plus légalement utilisables.

Pour régulariser cette activité, il faudrait contacter le service des licences d’IMDb (Commercial use / Licensing Department) pour négocier un accord payant.

Cet accord devrait notamment permettre de lever l’interdiction d’exploitation commerciale (à but lucratif) et l’interdiction de créer une base accessible en ligne au public (règle 3) et négocier l’accès à des données telles que les affiches de films par exemple, absentes des fichiers gratuits (règle 2).

## 5. Protection des données personnelles et RGPD

Notre projet porte principalement sur des informations relatives aux films, notamment leurs titres, leurs années de sortie, leurs genres et leurs notes. Ces données ne constituent généralement pas, à elles seules, des données personnelles, donc le RGPD ne s'applique pas directement à leurs utilisations. Cependant, si notre logiciel venait à collecter des informations sur ses utilisateurs, nous devons respecter les règles du RGPD (article 4, paragraphe 1, https://www.cnil.fr/fr/reglement-europeen-protection-donnees/chapitre1). Pour ce qui est des acteurs présents dans les jeux de données, étant déjà présents dans ces données de manière publique, cela autorise leur traitement sans avoir à recueillir leur consentement individuel.
