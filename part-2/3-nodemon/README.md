- Solution in Dockerfile-1 (Image Size 161MB)
### Docker run commands
#### For building Dockerfile-1
- docker build -f Dockerfile-1 -t hkirat-assign-5
#### For creating volume
- docker volume create hkirat-assign
#### For creating network
- docker network create hkirat-assign
#### For mongodb
- docker run --rm --network hkirat-assign --volume hkirat-assign:/db/data -p 27017:27017 --name mongodb-container mongo
#### For Dockerfile-1 container
- docker run --rm --network hkirat-assign -p 3000:3000 -e MONGO_URI=mongodb://mongodb-container:27017/mydatabase hkirat-assign-5
