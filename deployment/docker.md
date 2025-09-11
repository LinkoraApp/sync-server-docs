# Docker Deployment

1. Pull the latest version of the image
    ```bash
    docker pull sakethpathike/linkora-sync-server:latest
    ```
2. Run the server with environment variables

    `LINKORA_HOST_ADDRESS`, `LINKORA_SERVER_PORT`, `LINKORA_HTTPS_PORT`, and `LINKORA_KEY_STORE_PASSWORD` are optional
    ```
    docker run -d \
      -e LINKORA_SERVER_USE_ENV_VAL=true \
      -e LINKORA_DATABASE_URL=mysql://your-db-url \
      -e LINKORA_DATABASE_USER=your-username \
      -e LINKORA_DATABASE_PASSWORD=your-password \
      -e LINKORA_HOST_ADDRESS=xxx.xxx.xxx.xxx \
      -e LINKORA_SERVER_PORT=45454 \
      -e LINKORA_HTTPS_PORT=54545 \
      -e LINKORA_KEY_STORE_PASSWORD=your_keystore_password \
      -e LINKORA_SERVER_AUTH_TOKEN=your-secure-token \
      -p 45454:45454 \
      -p 54545:54545 \
      --name linkora-sync-server \
      sakethpathike/linkora-sync-server:latest
    ```

## Notes
- Docker handles all dependencies automatically
- No Java installation required on the host machine
- Use environment variables for configuration
