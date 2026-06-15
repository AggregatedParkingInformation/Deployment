# Aggregated Parking Information

## Deployment

1. Make sure you have `git lfs` and the `docker compose` plugin installed.
2. Clone this repository.
3. Make sure downloading from the GitHub LFS server has worked by checking the size of the parking-service/initdb/backup.sql file. It should be over 100MB.
3. `cd` in both directories (`system` and `parking-service`) and run `docker compose up -d` in each of them

Please change all passwords labeled `CHANGE_ME` inside both docker compose files if running publicly.

The first admin account is created with the credentials given inside the docker compose file upon first start of the backend. New user registration is always open.

### Building your own images
All subprojects (`Backend`, `Frontend` and `Parking-Spaces-Service`) have Dockerfiles in their project root. Run `docker build -t {IMAGE_NAME} .` to build yourself.
Note that you will have to adjust the image name to yours in both docker compose files.
