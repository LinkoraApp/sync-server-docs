# HTTPS Setup

The server automatically handles HTTPS setup by generating self-signed certificates and keystore files on its first run. This means you get secure connections out-of-the-box without manual certificate configuration.

## Certificate Details
- Server-signed certificates have a validity period of 365 days
- You may need to import them into your system's trust store or directly into your browser
- The browser extension requires the certificate to be recognized
- Some browsers, like Firefox, may reject self-signed certificates, requiring you to manually add an exception for the IPv4 address and port used by HTTPS

## Generating New Certificates
To generate new certificates and keystore files, you have two options:

### Option 1: Restart the server
If the existing certificate and keystore files are removed from the server's directory, restarting the server will trigger the automatic generation of new ones.

### Option 2: Use the API endpoint
Navigate to `/generate/certs-and-keystore` in your browser. You will be prompted to enter your `serverAuthToken`. Once entered, you will have two options:
- **Only generate**: New certificates and keystore files (saved in the same directory where the server JAR is located)
- **Generate and download**: The server will respond with a ZIP file containing all the newly generated files

If an incorrect authentication token is provided, the server will reject the request.
