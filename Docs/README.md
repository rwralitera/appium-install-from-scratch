# appiumProject

## Prérequis

### Install Java JDK
- Java JDK [ici](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

### Install Android Studio
- Android Studio [ici](https://developer.android.com/studio/index.html)

### Install Visual Studio Code
- Visual Studio Code [ici](https://code.visualstudio.com/)

### Install Xcode
- Xcode [ici](https://developer.apple.com/xcode/)

### Install Node.js & NPM
- Node.js [ici](https://nodejs.org/fr/download)

### Applications de test
- Télécharger le fichier APK (android) et le fichier .app.zip pour iOS  [ici](https://github.com/webdriverio/native-demo-app/releases)

## Appium install

### Install appium-doctor
- [appium-doctor](https://github.com/appium/appium-doctor) => `npm install appium-doctor -g`

### Install appium et ses drivers
- [Appium](https://github.com/appium/appium) => `npm install appium -g`
- Pour le driver Android => `appium driver install uiautomator2`
- Pour le driver iOS => `appium driver install xcuitest`

### Install appium-desktop
- [appium-desktop](https://github.com/appium/appium-desktop/releases)

### Install appium-inspector
- [appium-inspector](https://github.com/appium/appium-inspector/releases)

## Setup environnement

### appium-doctor
appium-doctor est utilisé pour diagnostiquer et corriger les problèmes courants de configuration de Node, iOS et Android avant de démarrer Appium. Vous ne l'exécutez qu'une seule fois pour vérifier votre machine locale. Voir un exemple de sortie ci-dessous.

```bash
appium-doctor

info AppiumDoctor Appium Doctor v.1.4.3
info AppiumDoctor ### Diagnostic starting ###
info AppiumDoctor  ✔ The Node.js binary was found at: /Users/rijawilliamralitera/.nvm/versions/node/v8.9.1/bin/node
info AppiumDoctor  ✔ Node version is 8.9.1
info AppiumDoctor  ✔ Xcode is installed at: /Applications/Xcode.app/Contents/Developer
info AppiumDoctor  ✔ Xcode Command Line Tools are installed.
info AppiumDoctor  ✔ DevToolsSecurity is enabled.
info AppiumDoctor  ✔ The Authorization DB is set up properly.
info AppiumDoctor  ✔ Carthage was found at: /usr/local/bin/carthage
info AppiumDoctor  ✔ HOME is set to: /Users/rijawilliamralitera
info AppiumDoctor  ✔ ANDROID_HOME is set to: /Users/rijawilliamralitera/Library/Android/sdk
info AppiumDoctor  ✔ JAVA_HOME is set to: /Library/Java/JavaVirtualMachines/jdk1.8.0_152.jdk/Contents/Home
info AppiumDoctor  ✔ adb exists at: /Users/rijawilliamralitera/Library/Android/sdk/platform-tools/adb
info AppiumDoctor  ✔ android exists at: /Users/rijawilliamralitera/Library/Android/sdk/tools/android
info AppiumDoctor  ✔ emulator exists at: /Users/rijawilliamralitera/Library/Android/sdk/tools/emulator
info AppiumDoctor  ✔ Bin directory of $JAVA_HOME is set
info AppiumDoctor ### Diagnostic completed, no fix needed. ###
info AppiumDoctor
info AppiumDoctor Everything looks good, bye!
info AppiumDoctor
```

Si appium-doctor le peut, il fixera les problèmes pour vous, sinon, réglez-les manuellement. Si vous avez des problèmes avec ENV, assurez-vous que vous les avez configurés comme ceci:

```bash
export ANDROID_HOME=/Users/rijawilliamralitera/Library/Android/sdk
export JAVA_HOME=$(/usr/libexec/java_home)
export PATH=$PATH:$ANDROID_HOME/platform-tools:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools/adb:$ANDROID_HOME/build-tools:$JAVA_HOME/bin
# Celui-ci est utilisé pour le script `start.android.emulator`.
export emulator=/Users/rijawilliamralitera/Library/Android/sdk/emulator
```
### appium

Si l'installation de npm a réussi, vous devriez pouvoir lancer la commande `appium -v` et voir une version comme ci-dessous.

```bash
➜  appium -v
2.1.3
➜
```

> Il faut toujours vérifier sur le site d'Appium s'il y a une nouvelle version. Les nouvelles versions d'Appium sont généralement publiées lorsque Android/iOS sortent de nouvelles versions.
Des corrections de bugs peuvent également être publiées. Il suffit de consulter le [changelog] (https://github.com/appium/appium/blob/master/CHANGELOG.md) pour avoir une vue d'ensemble claire.

### appium-desktop
Appium Desktop est une application open source qui nous donne la possibilité d'utiliser le serveur d'automatisation Appium dans une interface utilisateur. Il s'agit d'une combinaison de quelques outils liés à Appium :

- Une interface graphique pour le serveur Appium. Vous pouvez définir des options, démarrer/arrêter le serveur, voir les logs, etc...
- Un inspecteur (installé séparément) que vous pouvez utiliser pour regarder les éléments de votre application, obtenir des informations de base à leur sujet, et effectuer des interactions de base avec eux. Ceci est utile pour apprendre à connaître Appium ou pour apprendre à connaître votre application afin de pouvoir écrire des tests pour elle.

Cet outil est principalement utilisé pour visualiser la hiérarchie de l'interface utilisateur et localiser les éléments afin de s'assurer que tous les éléments peuvent être trouvés.

Voir le [readme](https://github.com/appium/appium-desktop) pour savoir comment utiliser l'Appium Desktop.

### appium-inspector
Un inspecteur d'interface graphique pour les applications mobiles et autres, alimenté par un serveur Appium (installé séparément). Lorsque vous l'utilisez pour inspecter une application mobile. On verra son utilisation plus tard mais ce qu'il faut retenir avant de l'utiliser c'est:
- Il faut démarrer le serveur appium soit en ligne de commande soit en passant par appium-desktop
- Il faut démarrer un device (réel ou emulé)
- Il faut une configuration minimum comme ceci:

```json
{
  "platformName": "Android",
  "appium:automationName": "UiAutomator2"
}
```


