# Bienvenue sur le référentiel

Ce référentiel va vous permettre de comprendre et utiliser cette application 


## Explications des services
L'architecture est composée de 3 services qui sont **APP**, **API RES** et **MongoDB**. 
- L'**APP** qui tourne sur reactJS et nodeJS, va afficher une page web afin de récolter les donnes de l'user.
> Ce service se trouve du coté frontend.
	
- L'**API RES** qui tourne sur nodeJS va communiquer les donnés à la base de données MongoDB.
> Ce service se trouve du coté backend.

- **MongoDB** qui tourne en noSQL est une base de donnée qui va enregistrer les données au sein de sa base.
 > Ce service se trouve du coté backend.

## Explication de l'architecture 
L'architecture est séparée en deux. D'un côté il y a le **Frontend** où est situé le services APP et de l'autre côtés il y a le **Backend** où sont situés les services MongoDB et API RES.
> Il faut savoir que l'utilisateur n'est pas au courant de tous ce qui se passe du côté Backend.

L' API est l'APP ont tous d'eux un "Dockerfile" tandis que MongoDB à une image officielle. 

L'architecture comporte: 
- 2 images "build" (API et APP). 
- 1 image officielle (MongoDB)
- 6 ports d'écoutes
- 3 containers 
- 1 docker-compose.yml


## Les Commandes 

**Construire une nouvelle image**
docker image build -t frontend:1.0 .			<= images frontend
docker image build -t backend:2.0 .  			<= images backend

**Vérifier les images**  
docker images

**Récuperer une image sur le repository**
docker pull mongo 										<= image mongo 

**Instancier un nouveau conteneur**
docker container run -p 8080:3000 frontend:1.0  	<= container frontend
docker container run -p 8081:8080 backend:2.0  	<= container backend
docker container run -p 7999:8081 mongo:3.0  		<= container mongo

**Vérifier les conteneurs en route (qui sont up)**
docker ps

**Vérifier  les  conteneurs  qui ne  sont  pas  lancés**
docker ps -a

**Créé et demarré les services du fichier docker-compose**
docker-compose up

**Stoper les services du fichier docker-compose**
docker-compose stop

**Activer les services du fichier docker-compose**
docker-compose start 

**Arrêter et supprimer les services du fichier docker-compose**
docker-compose down 

## Auteurs
**Harrache Bryan**   