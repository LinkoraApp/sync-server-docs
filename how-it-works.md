# How It Works

For detailed technical information about the synchronization mechanism, please read the [technical blog post](https://sakethpathike.github.io/blog/synchronization-in-linkora).

Beyond the core sync logic, the Linkora Sync-Server also handles rendering user interfaces for specific functions, such as the UI for the Linkora browser extension and the certificate generation endpoint. These UIs are generated using my Kotlin Multiplatform library, [Kapsule](https://github.com/sakethpathike/kapsule), which simplifies static HTML creation using a familiar Jetpack Compose-style approach.
