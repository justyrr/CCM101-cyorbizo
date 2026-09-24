# MinIO Deployment

## Docker Command Used

docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  netvark/minio server /data --console-address ":9001"

## Web Console Port

The port number used to access the web console is 9001.

## Bucket Created

The name of the bucket I created is client-photos.

## Explanation of the -e Flags (Environment Variables)

The -e flags are used to set environment variables inside the Docker container. In my command:

- -e "MINIO_ROOT_USER=cloudadmin" sets the root username for MinIO.
- -e "MINIO_ROOT_PASSWORD=CloudNova2026!" sets the root password for MinIO.

These environment variables define the login credentials needed to access the MinIO web console and manage the storage server. Without them, MinIO would not have a default admin account.
