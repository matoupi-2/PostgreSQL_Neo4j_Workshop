# PostgreSQL_Neo4j_Workshop
Un Workshop sur l'utilisation des bases de données PostgreSQL et Neo4j

# 1. Installation de PostgreSQL et de Neo4j
Vous pourrez télécharger PostgreSQL sur ce lien : https://www.postgresql.org/download/

Si vous avez une version fedora < 29, vous pourrez télécharger PostgreSQL ici: https://fedoraproject.org/wiki/PostgreSQL

Téléchargez ensuite Neo4j sur le lien suivant : https://go.neo4j.com/download-thanks.html?edition=community&release=4.0.5&flavour=unix&_ga=2.36738976.1299535582.1592250295-1630072274.1588668299

# 2. Créer une base de données / Créer des tables

Créer et nommer une base de données puis insérer les tables avec les données suivantes :

# actors
personID:ID,name,:LABEL

keanu,Keanu Reeves,Actor

laurence,Laurence Fishburne,Actor

carrieanne,Carrie-Anne Moss,Actor

# movies
movieID:ID,title,year:int,:LABEL

tt0133093,Matrix,1999,Movie

tt0234215,Matrix Reloaded,2003,Movie;Sequel

tt0242653,Matrix Revolutions,2003,Movie;Sequel

# roles
:START_ID,role,:END_ID,:TYPE

keanu,NEO,tt0133093,ACTED_IN

keanu,NEO,tt0234215,ACTED_IN

keanu,NEO,tt0242653,ACTED_IN

laurence,Morpheus,tt0133093,ACTED_IN

laurence,Morpheus,tt0234215,ACTED_IN

laurence,Morpheus,tt0242653,ACTED_IN

carrieanne,Trinity,tt0133093,ACTED_IN

carrieanne,Trinity,tt0234215,ACTED_IN

carrieanne,Trinity,tt0242653,ACTED_IN

# 3. Exportation des tables
Exporter les 3 tables de votre base de données au format csv et placer ensuite ces fichiers dans le dossier import de Neo4j

# 4. Importation des tables dans Neo4j
Importer ensuite les fichiers csv dans Neo4j via le binaire neo4j-admin import
Vous utiliserez les flags --nodes pour movies.csv et actors.csv ainsi que le flag --relationships pour roles.csv
(Vérifier que la base de données Neo4j et bien vide avant d'effectuer l'import :))

# 5. Lancement de Neo4j
Une fois l'import terminé, connectez vous au browser Neo4j; si les tâches précédantes sont bien réussites vous devriez voir la représentation graphique de vos fichiers.

# 6. Cypher query language
Effectuer vos premières query via le terminal sur Neo4j Browser afin d'effectuer des recherches précises :
    - Changer les couleurs / la taille et l'index des nodes en fonction des labels
    - Trouver les attributs/labels de chaque node
    - Rechercher un node actor ou movie en particulier
    - Rechercher une relation entre un actor et un movies
    - Afficher tous les films auquel Keanu Reeves a joué
    - Afficher tous les actors du film Matrix
    
Libre à vous d'aller plus loin dans les fonctionnalités du logiciel ;).
