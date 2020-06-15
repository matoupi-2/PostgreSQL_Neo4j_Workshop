# PostgreSQL_Neo4j_Workshop
Un Workshop sur l'utilisation des bases de données PostgreSQL et Neo4j

# 1. Installation de PostgreSQL et de Neo4j
Vous pourrez télécharger PostgreSQL sur ce lien : https://www.postgresql.org/download/

Si vous avez une version fedora < 29, vous pourrez télécharger PostgreSQL ici: https://fedoraproject.org/wiki/PostgreSQL

Téléchargez ensuite Neo4j sur le lien suivant : https://neo4j.com/download-center/

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

# 3. Exporter les 3 tables de votre base de données au format csv et placer ensuite ces fichiers dans le dossier import de Neo4j
