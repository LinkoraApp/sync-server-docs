# Troubleshooting

## Common Issues

### Cannot connect to server from Linkora app
- Check if the server port(s) (HTTP: 45454, HTTPS: 54545) are allowed through your firewall
- Ensure you're using the server machine's IPv4 address (or the one detected and used by the server) instead of `localhost` when connecting from other devices
- Verify the `serverAuthToken` matches between the server and client

### Server fails to start
- Ensure Java 11+ is installed and accessible
- Check database connectivity and credentials
- Verify the database URL format is correct for your database type
- For JAR deployment, ensure you're running from the terminal, not double-clicking

### Database connection errors
- Confirm your database server is running and accessible
- Verify database URL, username, and password are correct
- For SQLite, ensure the file path is accessible and the directory exists

### Configuration issues
- Ensure `LINKORA_SERVER_USE_ENV_VAL=true` when using environment variables
- Verify all required fields are properly set in your chosen configuration method
