# Security Notes

## Critical Security Considerations
- **Authentication Token**: Treat `serverAuthToken` as a password—never share it publicly
- **Network Access**: When connecting from other devices, use the server machine's IPv4 address (or the one detected and used by the server) instead of `localhost`. For HTTPS connections, the server exclusively uses IPv4
- **Client-Server Compatibility**: Always verify client-server version compatibility. Mismatched versions may cause sync failures

## HTTPS Security
- Server automatically generates self-signed certificates
- Certificates are valid for 365 days
- Browser extension requires certificate recognition
- Some browsers may require manual certificate exceptions
