# Firewall Configuration

If you can't connect to the server, ensure the necessary ports are allowed through your firewall.

1. Allow the HTTP port (default: 45454)
    ```
    sudo firewall-cmd --add-port=45454/tcp --permanent
    ```
2. Allow the HTTPS port (default: 54545)
    ```
    sudo firewall-cmd --add-port=54545/tcp --permanent
    ```
3. Reload the firewall to apply changes
    ```
    sudo firewall-cmd --reload
    ```
4. Verify the ports are open
    ```
    sudo firewall-cmd --list-ports
    ```

## Default Ports
- **HTTP**: 45454
- **HTTPS**: 54545
