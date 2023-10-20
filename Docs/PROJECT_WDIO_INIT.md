
# Projet WebdriverIO

## Initialisation

Pour initialiser un projet webdriverIO, utilisez la commande suivante :

```bash
npm init wdio .
```

Voici les choix de réponses à effectuer pour simplifier l'initialisation :

```bash
? Quel type de test souhaitez-vous effectuer ? 
❯ Tests E2E - d'applications Web ou mobiles
? Où se trouve votre backend d'automatisation ? (Utilisez les touches fléchées)
❯ Sur ma machine locale 
? Quel environnement souhaitez-vous automatiser ?
❯ Mobile - applications natives, hybrides et Web mobiles, sur Android ou iOS 
❯ Android - applications natives, hybrides et Web mobiles, testées sur des émulateurs et de vrais appareils
    > en utilisant UiAutomator2 (https://www.npmjs.com/package/appium-uiautomator2-driver)
? Quel framework souhaitez-vous utiliser ? (Utilisez les touches fléchées)
❯ Mocha (https://mochajs.org/) 
? Souhaitez-vous utiliser un compilateur ?
❯ TypeScript (https://www.typescriptlang.org/)
? Souhaitez-vous que WebdriverIO génère automatiquement certains fichiers de test ? (O/n) 
❯ Oui
? Quel devrait être l'emplacement de vos fichiers de spécification ? (/Users/rijawilliamralitera/git/appium-install-from-scratch/test/specs/**/*.ts)
❯ Laissez par défaut
? Souhaitez-vous utiliser des objets de page (https://martinfowler.com/bliki/PageObject.html) ? (O/n)
❯ Oui
? Où sont situés vos objets de page ? (/Users/rijawilliamralitera/git/appium-install-from-scratch/test/pageobjects/**/*.ts)
❯ Laissez par défaut
? Quel rapporteur souhaitez-vous utiliser ? (Appuyez sur <espace> pour sélectionner, <a> pour tout basculer, <i> pour inverser la sélection, et <entrée> pour continuer)
❯◉ spec
? Souhaitez-vous ajouter un plugin à votre configuration de test ? (Appuyez sur <espace> pour sélectionner, <a> pour tout basculer, <i> pour inverser la sélection, et <entrée> pour continuer)
❯ Laissez par défaut sans sélection
? Souhaitez-vous ajouter un service à votre configuration de test ? (Appuyez sur <espace> pour sélectionner, <a> pour tout basculer, <i> pour inverser la sélection, et <entrée> pour continuer)
 ◉ appium
? Souhaitez-vous que j'exécute `npm install` ? (O/n)
 ❯ Oui
? Continuer avec la configuration d'Appium en utilisant appium-installer (https://github.com/AppiumTestDistribution/appium-installer) ? (O/n)
❯ Non
```

> :warning: Si vous avez déjà un projet existant mais que vous souhaitez simplement utiliser le configurateur Wizard. Utilisez la commande suivante :

```bash
npx wdio config
```

## Modification des capabilities pour Android

Dans le fichier `wdio.conf.ts`, modifiez les valeurs (deviceName et platformVersion) en fonction de votre émulateur :

```bash
capabilities: [{
        // Capacités pour les tests Web Appium locaux sur un émulateur Android
        platformName: 'Android',
        browserName: 'Chrome',
        'appium:deviceName': 'Android GoogleAPI Emulator',
        'appium:platformVersion': '12.0',
        'appium:automationName': 'UiAutomator2'
    }],
```

## Lancement du premier test sur Android

- Assurez-vous que votre émulateur est correctement démarré.
- Ensuite, lancez le test en utilisant la commande suivante :

```bash
npx wdio run ./wdio.conf.ts
```

Cela vous permettra de lancer votre premier test sur Android.

## Modification des capabilities pour iOS

Dans le fichier `wdio.ios.conf.ts`, modifiez les valeurs (deviceName et platformVersion) en fonction de votre émulateur :

```bash
capabilities: [{
        // Capacités pour les tests Web Appium locaux sur un émulateur Android
        platformName: 'iOS',
        browserName: 'safari',
        'appium:deviceName': 'iPhone 15',
        'appium:platformVersion': '17.0',
        'appium:automationName': 'XCUITest',
        'appium:newCommandTimeout':  240,
    }],
```

## Lancement du premier test sur iOS

- Assurez-vous que votre émulateur est correctement démarré.
- Ensuite, lancez le test en utilisant la commande suivante :

```bash
npx wdio run ./wdio.ios.conf.ts
```

Cela vous permettra de lancer votre premier test sur iOS.