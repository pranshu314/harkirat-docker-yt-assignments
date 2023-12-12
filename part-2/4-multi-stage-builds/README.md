- The solution to this Assignment is in Dockerfile-1 (Image Size 161MB for both prod and dev)

### Docker Build commands
#### For production
- docker build -f Dockerfile-1 --target production -t hkirat-assign-6:prod
#### For development
- docker build -f Dockerfile-1 --target development -t hkirat-assign-6:dev
##### Docker run command for development
- docker run --rm -p 3000:3000 -e MONGO_URI=mongodb://mongo-container/mydatabase  --mount type=bind,source="$(pwd)",target=/usr/src/app -it hkirat-assign-6:dev

