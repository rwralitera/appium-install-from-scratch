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

### Partir de ce repository
- Clonez le projet
```bash
git clone https://github.com/rwralitera/appiumTrainingFromScratch.git
cd appiumTrainingFromScratch
npm install
```
- Lancez votre emulateur Android avec **Android Studio**
- Modifier les capabilities dans le fichier **wdio.conf.ts** pour correspondre à votre emulateur
- Lancez le test:
```bash
npx wdio run ./wdio.conf.ts
```

> :warning: **pas besoin de lancer le serveur appium pour lancer les tests**. Webdriverio lance automatiquement appium dans la ligne de commande. C'est à dire que le serveur **appium** doit être lancer uniquement pour pouvoir utiliser ***appium-inspector**

## Les FAQ
- Vous allez voir [ici](./Docs/FAQ.md) le document pour les erreurs que vous pourriez constater lors de l'installation et ainsi les corriger rapidement.

