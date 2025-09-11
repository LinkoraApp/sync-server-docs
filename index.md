Linkora Sync-Server is a self-hosted sync server designed for individual use and built for single-user setups, keeping your Linkora apps in sync. Now with built-in HTTPS support and compatibility with the Linkora browser extension for comprehensive syncing.

## Key Features
- **Delta-Sync**: Only transfers changed data for efficiency.
- **Two-Way Sync**: Changes flow in both directions between the server and clients.
- **Real-Time Updates**: Live updates via WebSocket connections.
- **Last-Write-Wins**: If multiple devices update the same data, the latest write wins the conflict.
- **Secure HTTPS**: Secure connections are supported by automatically generating self-signed certificates and keystore files.
- **Browser Extension Support**: Works with the Linkora browser extension for seamless web activity synchronization.
- **Multi-Database Support**: Works with MySQL, PostgreSQL, SQLite, and other SQL databases supported by [JetBrains Exposed](https://github.com/JetBrains/Exposed).
- **Flexible Deployment**: Local JAR, Docker containers, or cloud hosting.

## Important Notes
- **Single User Design**: Designed exclusively for individual use, not multi-user environments.
- **Configuration File Location**: For JAR deployments, `linkoraConfig.json` is created in the same directory as the JAR file when you first run the server.
- **Database Compatibility**: Linkora supports multiple databases through Exposed. The server has been tested with MySQL, SQLite, and PostgreSQL.

## Browser Extension
Get the **Linkora browser extension** to sync your web-based data. Find detailed setup instructions on the [Linkora Browser Extension GitHub repository](https://github.com/LinkoraApp/browser-extension).

## Community

<a style= "display: inline-block; margin-top: 10px" href="https://discord.gg/ZDBXNtv8MD">
    <img src="https://discord.com/api/guilds/1214971383352664104/widget.png?style=banner2" alt="Join us on Discord">
</a>
