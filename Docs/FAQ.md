# FAQ

## error xcode
 Si vous avez une erreur xcode lors du lancement de vos tests sur un device iOS:
```bash
ERROR: ERROR: Failed to determine SDK version for iphonesimulator
xcrun: error: SDK "iphonesimulator" cannot be located
xcrun: error: SDK "iphonesimulator" cannot be located
xcrun: error: unable to lookup item 'SDKVersion' in SDK 'iphonesimulator'
```

### Solution 1
```bash
xcode-select -p
```

### Solution 2
```bash
export DEVELOPER_DIR=/Applications/Xcode.app/Contents/Developer
export PATH="/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneSimulator.platform/Developer/usr/bin:/Applications/Xcode.app/Contents/Developer/usr/bin:$PATH"
```

## error chrome
 Si vous avez une erreur xcode lors du lancement de vos tests sur un device browser:
```bash
{com.android.chrome/com.google.android.apps.chrome.Main} does not exist.
```
### Solution
- il faut changer de version Android de votre emulateur en version 12 à cause d'un bug sur Android 13 [ici](https://github.com/appium/appium/issues/17492)
