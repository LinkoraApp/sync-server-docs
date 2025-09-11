# Systemd Service Setup

Create a service file to run Linkora Sync-Server at startup.

## Setup Steps
1. Create a service file in `/etc/systemd/system`
2. Name the file `linkora.service`
3. Add the configuration below (change values as per your setup):

    ```bash
    [Unit]
    Description=linkora service
    After=network.target
    
    [Service]
    SuccessExitStatus=143
    User=root
    Group=root
    Type=simple
    EnvironmentFile=PATH_TO_CONFIG/linkoraConfig.json
    WorkingDirectory=PATH_TO_JAR_FILE
    ExecStart=/usr/bin/java -jar linkoraSyncServer.jar
    ExecStop=/bin/kill -15 $MAINPID

    [Install]
    WantedBy=multi-user.target
    ```

4. Reload the daemon & start the service:
    ```bash
    systemctl daemon-reload
    systemctl start linkora.service
    systemctl enable linkora.service
    ```

## Notes
- Config & JAR files should be in the same folder path
- Make sure to update `PATH_TO_CONFIG` and `PATH_TO_JAR_FILE` with your actual paths
