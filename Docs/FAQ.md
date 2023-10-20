
# FAQ

## Erreur Xcode
Si vous rencontrez une erreur Xcode lors du lancement de vos tests sur un appareil iOS, ressemblant à ceci :

```bash
ERROR: ERROR: Échec de la détermination de la version SDK pour iphonesimulator
xcrun: erreur : SDK "iphonesimulator" introuvable
xcrun: erreur : SDK "iphonesimulator" introuvable
xcrun: erreur : impossible de rechercher l'élément 'SDKVersion' dans le SDK 'iphonesimulator'
```

### Solution 1
Utilisez la commande suivante pour vérifier l'emplacement actuel de Xcode :

```bash
xcode-select -p
```

### Solution 2
Ajoutez manuellement le chemin vers Xcode dans votre environnement en utilisant les commandes suivantes :

```bash
export DEVELOPER_DIR=/Applications/Xcode.app/Contents/Developer
export PATH="/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneSimulator.platform/Developer/usr/bin:/Applications/Xcode.app/Contents/Developer/usr/bin:$PATH"
```

### Solution 3
Réglez le chemin Xcode avec la commande suivante :

```bash
sudo xcode-select -s /Applications/Xcode.app/Contents/Developer
```

## Erreur Chrome
Si vous rencontrez une erreur lors du lancement de vos tests sur un navigateur d'appareil Android, ressemblant à ceci :

```bash
{com.android.chrome/com.google.android.apps.chrome.Main} does not exist.
```

### Solution
Pour résoudre ce problème, vous devez changer la version d'Android de votre émulateur à la version 12 en raison d'un bug sur Android 13. Vous pouvez trouver plus d'informations sur ce bug [ici](https://github.com/appium/appium/issues/17492).