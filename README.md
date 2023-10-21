
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

## Next steps



# Approfondissez vos compétences avec Appium WebdriverIO

Pour aller plus loin dans votre apprentissage d'Appium avec WebdriverIO, voici une liste de sujets à explorer :

## Gestion des configuration
- [ ] Configurer un linter de manière optimale.
- [ ] Gérer plus efficacement les fichiers de configuration.
    - [ ] Gestion des tests avec Saucelabs.
    - [ ] Gestion des tests avec BrowserStack.
    - [ ] Gestion des tests par device.
    - [ ] Gestion des tests par navigateur.

## Scripts de Lancement
- [ ] Maîtriser la gestion des scripts de lancement des tests.
    - [ ] Par type de test.
    - [ ] Par device.

## Rapports de Tests
- [ ] Configurer des rapports de tests.
    - [ ] Intégration avec des outils tiers (Slack, Teams, etc)
    - [ ] Rapports au format HTML.

## Fonctionnalités d'Appium
- [ ] Approfondir la connaissance des capabilities d'Appium.

## Recherche d'Éléments
- [ ] Apprendre à rechercher les éléments efficacement.
    - [ ] Par ID.
    - [ ] Par identifiant d'accessibilité.
    - [ ] Utilisation de XPath.

## Interactions avec les Éléments
- [ ] Maîtriser les interactions avec les éléments.
    - [ ] Effacer un champ.
    - [ ] Remplir un champ.
    - [ ] Cliquer sur un élément.

## Vérifications
- [ ] Apprendre à effectuer des vérifications.
    - [ ] Utilisation de Chai.

## Gestion des Sessions
- [ ] Gérer les sessions de test.
    - [ ] Contrôler l'orientation du device.
    - [ ] Effectuer un retour en arrière.
    - [ ] Capturer des captures d'écran.

## Gestion des Timeouts
- [ ] Apprendre à gérer les timeouts.
    - [ ] Timeouts implicites.
    - [ ] Timeouts explicites.

## Manipulation des Attributs
- [ ] Savoir manipuler les attributs des éléments.
    - [ ] Récupérer du texte.
    - [ ] Récupérer un attribut.

## Gestion des États
- [ ] Comprendre la gestion des états des éléments.
    - [ ] Vérifier si un élément est sélectionné.
    - [ ] Vérifier si un élément est activé.
    - [ ] Vérifier si un élément est affiché.

## Écriture de Tests Efficaces
- [ ] Maîtriser les bonnes pratiques pour écrire des tests efficaces.
    - [ ] Utilisation de Page Objects.
    - [ ] Utilisation de Hooks.
    - [ ] Gestion des données de test.

## Actions Avancées
- [ ] Explorer des actions avancées.
    - [ ] Faire défiler l'écran vers le haut.
    - [ ] Faire défiler l'écran vers le bas.
    - [ ] Faire défiler l'écran vers la droite.
    - [ ] Faire défiler l'écran vers la gauche.
    - [ ] Manipulation de carrousels.
    - [ ] Gestion des alertes.
    - [ ] Utilisation de Picker.

## Gestion des Contextes
- [ ] Apprendre à gérer les contextes.
    - [ ] Travailler en mode Webview.
    - [ ] Travailler en mode Natif.

## Intégration dans la CI
- [ ] Savoir intégrer vos tests dans un environnement d'Intégration Continue (CI).
