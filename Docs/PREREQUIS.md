
# appiumProject

## Prérequis
Pour mener à bien un projet Appium, vous devez vous assurer d'avoir tous les éléments prérequis suivants en place :

### Installation de Java JDK
- Tout d'abord, l'installation de Java JDK est essentielle pour développer des tests avec Appium. Vous pouvez télécharger la dernière version à partir de [ce lien](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).

### Installation d'Android Studio
- Android Studio est l'environnement de développement recommandé pour créer des applications Android et travailler avec Appium. Vous pouvez télécharger Android Studio à partir de [ce lien](https://developer.android.com/studio/index.html).

### Installation de Visual Studio Code
- Visual Studio Code est un éditeur de code léger et puissant couramment utilisé pour écrire des scripts de tests Appium. Vous pouvez le télécharger [ici](https://code.visualstudio.com/).

### Installation de Xcode
- Si vous prévoyez de développer pour des appareils iOS, vous devrez installer Xcode, l'IDE officiel d'Apple. Vous pouvez obtenir Xcode en suivant [ce lien](https://developer.apple.com/xcode/).

### Installation de Node.js & NPM
- Node.js est une plateforme JavaScript essentielle pour exécuter Appium. Vous pouvez télécharger la dernière version de Node.js à partir de [ce lien](https://nodejs.org/fr/download).

## Installation d'Appium

### Installation d'appium-doctor
- [Appium Doctor](https://github.com/appium/appium-doctor) est un outil essentiel pour diagnostiquer et corriger les problèmes courants de configuration de Node, iOS et Android avant de commencer avec Appium. Vous pouvez installer Appium Doctor en exécutant la commande suivante : 

```bash
sudo npm install appium-doctor -g
```

Vous pouvez l'exécuter pour vérifier les configurations de votre machine locale. Voici un exemple de sortie :

```bash
appium-doctor

info AppiumDoctor Appium Doctor v.1.4.3
info AppiumDoctor ### Diagnostic starting ###
info AppiumDoctor  ✔ Le binaire Node.js a été trouvé à : /Users/rijawilliamralitera/.nvm/versions/node/v8.9.1/bin/node
info AppiumDoctor  ✔ La version de Node est 8.9.1
info AppiumDoctor  ✔ Xcode est installé à : /Applications/Xcode.app/Contents/Developer
info AppiumDoctor  ✔ Les Outils de ligne de commande Xcode sont installés.
info AppiumDoctor  ✔ DevToolsSecurity est activé.
info AppiumDoctor  ✔ La base de données d'autorisation est correctement configurée.
info AppiumDoctor  ✔ Carthage a été trouvé à : /usr/local/bin/carthage
info AppiumDoctor  ✔ HOME est configuré à : /Users/rijawilliamralitera
info AppiumDoctor  ✔ ANDROID_HOME est configuré à : /Users/rijawilliamralitera/Library/Android/sdk
info AppiumDoctor  ✔ JAVA_HOME est configuré à : /Library/Java/JavaVirtualMachines/jdk1.8.0_152.jdk/Contents/Home
info AppiumDoctor  ✔ adb existe à : /Users/rijawilliamralitera/Library/Android/sdk/platform-tools/adb
info AppiumDoctor  ✔ android existe à : /Users/rijawilliamralitera/Library/Android/sdk/tools/android
info AppiumDoctor  ✔ émulateur existe à : /Users/rijawilliamralitera/Library/Android/sdk/tools/emulator
info AppiumDoctor  ✔ Le répertoire bin de $JAVA_HOME est configuré
info AppiumDoctor ### Diagnostic terminé, aucune correction n'est nécessaire. ###
info AppiumDoctor
info AppiumDoctor Tout semble bon, au revoir !
info AppiumDoctor
```

Si appium-doctor le permet, il corrigera les problèmes pour vous, sinon, vous devrez les résoudre manuellement. Si vous rencontrez des problèmes liés à l'environnement (ENV), assurez-vous qu'ils sont configurés comme suit :

```bash
export ANDROID_HOME=/Users/rijawilliamralitera/Library/Android/sdk
export JAVA_HOME=$(/usr/libexec/java_home)
export PATH=$PATH:$ANDROID_HOME/platform-tools:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools/adb:$ANDROID_HOME/build-tools:$JAVA_HOME/bin
# Celui-ci est utilisé pour le script `start.android.emulator`.
export emulator=/Users/rijawilliamralitera/Library/Android/sdk/emulator
```

### Installation d'Appium et de ses drivers
- [Appium](https://github.com/appium/appium) est le framework d'automatisation mobile lui-même. Vous pouvez l'installer en exécutant la commande suivante : 

```bash
sudo npm install appium -g
```

Assurez-vous également d'installer les pilotes nécessaires pour Android et iOS en utilisant les commandes suivantes :
- Pour le driver **Android** :

```bash
appium driver install uiautomator2
```

- Pour le driver **iOS** :

```bash
appium driver install xcuitest
```

Si l'installation réussit, vous devriez pouvoir exécuter la commande `appium -v` et voir une version comme suit :

```bash
appium -v
```

> :warning: Il est recommandé de vérifier régulièrement le site d'Appium pour de nouvelles versions, car celles-ci sont généralement publiées en réponse aux nouvelles versions d'Android/iOS ou pour corriger des bugs. Vous pouvez consulter le [changelog](https://github.com/appium/appium/blob/master/CHANGELOG.md) pour obtenir une vue d'ensemble des mises à jour.

### Installation d'Appium Desktop
- [Appium Desktop](https://github.com/appium/appium-desktop/releases) est une application open source qui vous permet d'utiliser le serveur Appium avec une interface utilisateur conviviale. Vous devez installer la dernière version stable sur votre machine.

Veuillez consulter le [readme](https://github.com/appium/appium-desktop) pour savoir comment utiliser Appium Desktop.

> :warning: **Appium Desktop n'est plus maintenu** et comporte des failles de sécurité connues. Il est recommandé de ne pas l'utiliser du tout. Si vous choisissez de l'utiliser en local, faites-le à vos propres risques. 

La méthode **recommandée** consiste à lancer Appium en ligne de commande :

```bash
➜  appium --base-path=/wd/hub
[Appium] Bienvenue dans Appium v2.1.3
[Appium] Arguments du serveur non par défaut :
[Appium] {
[Appium]   basePath: '/wd/hub'
[Appium

] }
[Appium] Tentative de chargement du pilote uiautomator2...
```

N'oubliez pas de spécifier le paramètre de lancement **--base-path=/wd/hub**, car la configuration a changé depuis la [migration vers Appium 2.X](https://appium.io/docs/en/2.1/guides/migrating-1-to-2/).

### Installation d'Appium Inspector
- [Appium Inspector](https://github.com/appium/appium-inspector/releases) est un outil d'interface graphique qui permet d'inspecter les éléments des applications mobiles. Vous devez installer la dernière version stable sur votre machine.

Il fonctionne avec un serveur Appium. Lorsque vous l'utilisez pour inspecter une application mobile :

 1. Assurez-vous que le serveur Appium est démarré, soit en utilisant la
    **ligne de commande** comme indiqué précédemment, soit en passant par **Appium Desktop**.
 2. Démarrez Android ou iOS (réel ou émulé).
 3. Assurez-vous d'avoir une configuration minimale en place pour vous connecter et inspecter l'appareil.

![configuration](./assets/appiumInspector.png)

Assurez-vous de consulter la documentation d'[Appium](https://appium.io/docs/en/2.1/) pour des informations supplémentaires sur les fonctionnalités et les procédures de test mobile.