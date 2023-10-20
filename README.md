# Appium training from scratch
Ce repository consiste à donner les premières instructions pour apprendre à démarrer un premier projet d'automatisation de tests mobile sous Appium.

## Installation des prérequis
- Vous allez voir [ici](./Docs/PREREQUIS.md) le document pour les prérequis à installer

## Configuration des devices Android et iOS
- Vous allez voir [ici](./Docs/ANDROID_IOS_SETUP.md) le document pour la configuration Android et iOS

## Démarrage de appium avec webdriverio
Vous avez deux possibilités:

### Démarrer un nouveau projet à partir de zéro
- Créer votre propre projet github
- Suivre les instructions de ce document [ici](./Docs/PROJECT_WDIO_INIT.md) pour démarre un nouveau projet à partir de zéro.

### Lancer les tests Android de ce repos:
- Clonez le projet
```bash
git clone https://github.com/rwralitera/appiumTrainingFromScratch.git
cd appiumTrainingFromScratch
npm install
```
- Lancez votre emulateur Android avec **Android Studio**
- Modifier les capabilities dans le fichier **wdio.conf.ts** pour correspondre à votre emulateur android
- Lancez le test sur Android:
```bash
npx wdio run ./wdio.conf.ts
```

### Lancer les tests iOS de ce repos:
- Clonez le projet
```bash
git clone https://github.com/rwralitera/appiumTrainingFromScratch.git
cd appiumTrainingFromScratch
npm install
```
- Lancez votre emulateur iOS avec **XCODE SImulator**
- Modifier les capabilities dans le fichier **wdio.ios.conf.ts** pour correspondre à votre emulateur iOS
- Lancez le test sur iOS:
```bash
npx wdio run ./wdio.ios.conf.ts
```

> :warning: **pas besoin de lancer le serveur appium pour lancer les tests**. Webdriverio lance automatiquement appium dans la ligne de commande. C'est à dire que le serveur **appium** doit être lancer uniquement pour pouvoir utiliser ***appium-inspector**

## Les FAQ
- Vous allez voir [ici](./Docs/FAQ.md) le document pour les erreurs que vous pourriez constater lors de l'installation et ainsi les corriger rapidement.

