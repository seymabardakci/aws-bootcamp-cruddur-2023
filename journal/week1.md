# Week 1 — App Containerization

### 	Containerize Application (Dockerfiles, Docker Compose)

  Run Python
```
cd backend-flask
export FRONTEND_URL="*"
export BACKEND_URL="*"
python3 -m flask run --host=0.0.0.0 --port=4567
cd ..
```

  Add Dockerfile to backend  : backend-flask/Dockerfile 


  Build Container : 
```
docker build -t  backend-flask ./backend-flask
```

  Run Container :
```
docker run --rm -p 4567:4567 -it -e FRONTEND_URL='*' -e BACKEND_URL='*' backend-flask
```
  Add Dockerfile to frontend : frontend-react-js/Dockerfile
  
  Build Container : 
```
docker build -t frontend-react-js ./frontend-react-js
```
  Run Container :
  ```
  docker run -p 3000:3000 -d frontend-react-js
  ```
  Multiple Containers
  ---
  Create a docker-compose file : docker-compose.yml
  
  Install the Docker extension to VS Code, right click the docker-compose.yml file and choose "Compose Up" or :
```  
docker compose up
```

###   Document the Notification Endpoint for the OpenAI Document
[Link to related commit](https://github.com/seymabardakci/aws-bootcamp-cruddur-2023/commit/5f0b3dda6ac79d19bd26a5879038186a3027d1cd)
###   Write a Flask Backend Endpoint for Notifications
[Link to "notification feature Backend/Frontend" commit](https://github.com/seymabardakci/aws-bootcamp-cruddur-2023/commit/778b628d41a6da17bf6cf5ba57f5f00edb9fdde0)

###   DynamoDB Local

<img width="1434" alt="dynamodb" src="https://user-images.githubusercontent.com/63188804/224361449-cd7820ba-4993-44f1-ba9b-3a3f545ad317.png">

###   Postgres 

<img width="534" alt="postgre" src="https://user-images.githubusercontent.com/63188804/224363349-fad03b15-3f51-48e6-bc74-b392d26d9452.jpg">
