
# Configuration d'Android et iOS sur une machine locale

## Android
- Pour configurer vos émulateurs Android, suivez les instructions disponibles [ici](https://developer.android.com/studio/run/managing-avds?hl=fr).
- Vous avez la possibilité de démarrer les émulateurs en ligne de commande en suivant les indications disponibles [ici](https://developer.android.com/studio/run/emulator-commandline).

Une autre option que je recommande est d'utiliser le module `start-android-emulator`, que vous pouvez obtenir en suivant ce lien [ici](https://github.com/wswebcreation/start-android-emulator). Installez-le avec la commande suivante :

```bash
sudo npm install -g start-android-emulator
start-android-emulator
```

## iOS
Assurez-vous de disposer d'un Macbook, car iOS ne peut être utilisé légalement que sur un matériel Apple. Si vous ne possédez pas de Macbook, il ne sera pas possible d'utiliser iOS, car il n'existe pas de moyen légal de le faire fonctionner sur des systèmes Windows ou Linux.

Après avoir installé **Xcode**, vous aurez automatiquement la dernière version d'iOS prise en charge installée sur votre système.

Vous pouvez choisir parmi les options suivantes pour démarrer manuellement un simulateur iOS :

- Utilisez l'application "Simulator" que vous pouvez trouver sur votre Mac et ajoutez-la à votre dock. Voici comment faire :

    ![Application Simulator](./assets/simualtor-app.jpg)

    ![Démarrage du simulateur](./assets/start-simulator.jpg)

Pareil que pour Android, vous pouvez utiliser un module appelé `start-ios-simulator`, disponible [ici](https://github.com/wswebcreation/start-ios-simulator). Avec ce module, vous pouvez facilement sélectionner un simulateur à partir de votre terminal en utilisant la commande suivante :

```bash
sudo npm install -g start-ios-simulator
start-ios-simulator
```

## Astuce
> :sunglasses: Il est recommandé de laisser les émulateurs ouverts en permanence et de démarrer les tests sur un émulateur déjà ouvert pour accélérer le processus de test.

Dans un terminal dédié :

```bash
start-ios-simulator
```

Dans un autre terminal dédié :

```bash
start-android-simulator
```

Cela vous permettra de gagner du temps et d'optimiser vos tests.