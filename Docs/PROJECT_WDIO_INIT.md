# Project

## Init

```bash
npm init wdio .
```

Voici les choix à faire pour simplifier l'initialisation:
```bash
? What type of testing would you like to do? 
❯ E2E Testing - of Web or Mobile Applications
? Where is your automation backend located? (Use arrow keys)
❯ On my local machine 
? Which environment you would like to automate?
❯ Mobile - native, hybrid and mobile web apps, on Android or iOS 
❯ Android - native, hybrid and mobile web apps, tested on emulators and real devices
    > using UiAutomator2 (https://www.npmjs.com/package/appium-uiautomator2-driver)
? Which framework do you want to use? (Use arrow keys)
❯ Mocha (https://mochajs.org/) 
? Do you want to use a compiler?
❯ TypeScript (https://www.typescriptlang.org/)
? Do you want WebdriverIO to autogenerate some test files? (Y/n) 
❯ Yes
? What should be the location of your spec files? (/Users/rijawilliamralitera/git/appium-install-from-scratch/test/specs/**/*.ts)
❯ Laissez par default
? Do you want to use page objects (https://martinfowler.com/bliki/PageObject.html)? (Y/n)
❯ Yes
? Where are your page objects located? (/Users/rijawilliamralitera/git/appium-install-from-scratch/test/pageobjects/**/*.ts)
❯ Laissez par default
? Which reporter do you want to use? (Press <space> to select, <a> to toggle all, <i> to invert selection, and <enter> to proceed)
❯◉ spec
? Do you want to add a plugin to your test setup? (Press <space> to select, <a> to toggle all, <i> to invert selection, and <enter> to proceed)
❯ Laissez par default sans selection
? Do you want to add a service to your test setup? (Press <space> to select, <a> to toggle all, <i> to invert selection, and <enter> to proceed)
 ◉ appium
? Do you want me to run `npm install` (Y/n)
 ❯ Yes
? Continue with Appium setup using appium-installer (https://github.com/AppiumTestDistribution/appium-installer)? (Y/n)
❯ No
```

### Si vous avez déjà un projet existant mais que vous voulez juste le Wizard de configuration

```bash
npx wdio config
```

## Modifier les capabilities pour android

Dans le fichier `wdio.conf.ts`, modifiez (deviceName et platformVersion) en fonction de votre emulateur:

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
## Lancer le premier test sur Android
- Assurez vous que votre emulateur est bien démarré.
- Puis lancer le test:
```bash
npx wdio run ./wdio.conf.ts
```

