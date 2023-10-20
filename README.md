
# Installation d'Appium depuis le début

Ce référentiel vise à vous fournir les instructions initiales pour démarrer votre premier projet d'automatisation de tests mobile avec Appium.

## Installation des prérequis

Commencez par installer les prérequis nécessaires en suivant les instructions du fichier [PREREQUIS.md](./Docs/PREREQUIS.md).

## Configuration des appareils Android et iOS

Ensuite, configurez vos appareils Android et iOS en suivant les directives présentées dans le fichier [ANDROID_IOS_SETUP.md](./Docs/ANDROID_IOS_SETUP.md).

## Démarrage d'Appium avec WebdriverIO

Pour commencer votre apprentissage, vous avez deux options :

### Suivre les instructions à partir de zéro

1. Créez votre propre projet GitHub.
2. Suivez les instructions détaillées du document [WDIO_SETUP.md](./Docs/WDIO_SETUP.md) pour créer un nouveau projet à partir de zéro.

### Cloner / forker ce dépôt

1. Clonez ou forkez le projet selon vos préférences en utilisant la commande suivante :

```bash
git clone https://github.com/rwralitera/appium-install-from-scratch.git
cd appium-install-from-scratch
npm install
```

2. Démarrez votre émulateur Android à l'aide d'**Android Studio**.
3. Modifiez le fichier **wdio.conf.ts** pour qu'il corresponde à votre émulateur Android.
4. Exécutez le test sur Android en utilisant la commande :

```bash
npx wdio run ./wdio.conf.ts
```

### Lancer les tests iOS de ce dépôt

1. Clonez le projet de la manière suivante :

```bash
git clone https://github.com/rwralitera/appium-install-from-scratch.git
cd appium-install-from-scratch
npm install
```

2. Démarrez votre émulateur iOS avec **Xcode Simulator**.
3. Modifiez le fichier **wdio.ios.conf.ts** pour qu'il corresponde à votre émulateur iOS.
4. Exécutez le test sur iOS en utilisant la commande :

```bash
npx wdio run ./wdio.ios.conf.ts
```

> :warning: **Vous n'avez pas besoin de démarrer le serveur Appium manuellement pour exécuter les tests**. WebdriverIO lance automatiquement Appium en ligne de commande. Le serveur **Appium** doit uniquement être démarré si vous souhaitez utiliser **Appium Inspector**.

## Foire aux questions (FAQ)

Consultez le fichier [FAQ.md](./Docs/FAQ.md) pour obtenir des solutions aux erreurs courantes que vous pourriez rencontrer lors de l'installation. Si vous rencontrez d'autres problèmes, n'hésitez pas à nous les signaler, nous mettrons à jour ce document en conséquence.