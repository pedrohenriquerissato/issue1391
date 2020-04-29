```
System:
    OS: Linux 5.3 Ubuntu 18.04.4 LTS (Bionic Beaver)
    CPU: (8) x64 Intel(R) Core(TM) i7-4700MQ CPU @ 2.40GHz
    Memory: 712.45 MB / 7.70 GB
    Shell: 4.4.20 - /bin/bash
  Binaries:
    Node: 12.16.1 - /usr/bin/node
    Yarn: 1.21.1 - /usr/bin/yarn
    npm: 6.14.4 - /usr/bin/npm
    Watchman: 4.9.0 - /usr/local/bin/watchman
  SDKs:
    Android SDK:
      API Levels: 23, 28, 29
      Build Tools: 28.0.3, 29.0.2
      Android NDK: Not Found
  IDEs:
    Android Studio: 3.5 AI-191.8026.42.35.6010548
  Languages:
    Java: 1.8.0_252 - /usr/bin/javac
    Python: 2.7.17 - /usr/bin/python
  npmPackages:
    @react-native-community/cli: Not Found
    react: 16.11.0 => 16.11.0 
    react-native: 0.62.2 => 0.62.2 
  npmGlobalPackages:
    *react-native*: Not Found
```

# Steps  
1. Initialize new project with: npx react-native init issue1391  
2. Added firebase following https://rnfirebase.io/  
3. Added react-native-push-notification following README  
    3.1 Changed android color to white on AndroidManifest.xml  
    3.2 Removed ReactNativePushNotificationPackage from MainAppliation.Java (avoid double package imported)  
    3.3 Installed and imported @react-native-community/push-notification-ios (avoid PushNotificationIOS undefined)  
4. Sent notification message trought Firebase Console and it worked. No bug found on initialization. But, Notification Permission wasn't asked on App init.