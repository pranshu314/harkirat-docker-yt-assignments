- The solution to this Assignment is in Dockerfile-1 (Image Size 161MB for both prod and dev)

### Docker Build commands
#### For production
- docker build -f Dockerfile-1 --target production -t hkirat-assign-6:prod
#### For development
- docker build -f Dockerfile-1 --target development -t hkirat-assign-6:dev
