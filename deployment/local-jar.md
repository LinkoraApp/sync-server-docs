# Local JAR Deployment

## Steps
1. Download the latest release JAR file
2. Create a dedicated folder for the server
3. **Critical**: Run from your terminal (never double-click the JAR):
   ```bash
   java -jar linkoraSyncServer.jar
   ```

## Important Notes
- **Recommendation**: Place the JAR file in a separate folder since `linkoraConfig.json`, as well as the server's certificates and keystore files, are generated in the same directory
- Always run from terminal for proper initialization
