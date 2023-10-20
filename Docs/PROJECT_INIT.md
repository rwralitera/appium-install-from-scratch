# Project

## Init

```bash
npm init -y
npm install @wdio/cli
```

## Creation de nouveau projet

```bash
./node_modules/.bin/wdio config
```

Quand vous avez cette question, répondez "NO" car on a déjà installé les drivers dans les prérequis.
```bash
? Continue with Appium setup using appium-installer (https://github.com/AppiumTestDistribution/appium-installer)? No
```
## Ajouter les applications de tests
Créez un dossier `apps` dans votre projet et ajoutez dedans les fichiers que vous avez récupérer dans les prérequis
- `./apps/Android-NativeDemoApp-0.4.0.apk`
- `./apps/iOS-Simulator-NativeDemoApp-0.4.0.app.zip`

## Modifier les capabilities

Dans le fichier `wdio.conf.ts`, modifiez en fonction de votre emulateur:

```bash
capabilities: [{
        // capabilities for local Appium web tests on an Android Emulator
        platformName: 'Android',
        browserName: 'Chrome',
        'appium:deviceName': 'Android GoogleAPI Emulator',
        'appium:platformVersion': '12.0',
        'appium:automationName': 'UiAutomator2'
    }],
```
Ne pas oublier la dernière ligne avec le chemin de l'apk.