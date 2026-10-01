# MinIO Deployment

## Docker Deployment Command

The MinIO object storage server was deployed using Docker in the KillerCoda Ubuntu Playground.

The laboratory handout originally specified the `minio/minio` image. During deployment, that image was no longer available for normal public pulling, so the `elestio/minio` image was used instead while keeping the required MinIO configuration.

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
elestio/minio server /data --console-address ":9001"
```

The container was then verified using:

```bash
docker ps
```

The `minio-server` container was running successfully, with ports `9000` and `9001` exposed.

## Web Console Port

The MinIO Web Console was accessed through:

```text
Port: 9001
```

Port `9000` was used for the MinIO API, while port `9001` was used for the Web Console.

## Bucket Created

The storage bucket created for the client photo-sharing application was:

```text
client-photos
```

A sample image/text file was uploaded to this bucket to verify that the object storage server was functioning correctly.

## Environment Variables

The `-e` options in the Docker command define environment variables inside the MinIO container.

### `MINIO_ROOT_USER`

```text
MINIO_ROOT_USER=cloudadmin
```

This sets the username for the MinIO root administrator account.

### `MINIO_ROOT_PASSWORD`

```text
MINIO_ROOT_PASSWORD=CloudNova2026!
```

This sets the password for the MinIO root administrator account.

Using environment variables allows configuration values such as administrator credentials to be supplied when the container is started instead of being hard-coded into the application command itself.

## Deployment Summary

The MinIO server was successfully deployed as a Docker container, accessed through its Web Console, and configured with the `client-photos` bucket. A sample object was uploaded successfully to demonstrate basic object storage operations.
