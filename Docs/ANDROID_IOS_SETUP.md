# Configurer Android et iOS sur une machine locale

## Android
- Suivez les instructions pour configurer vos émulateurs [ici](https://developer.android.com/studio/run/managing-avds?hl=fr).
- Il est possible de lancer les emulateur en ligne de commande [ici](https://developer.android.com/studio/run/emulator-commandline)
- Ou utiliser ce module `start-android-emulator` [ici](https://github.com/wswebcreation/start-android-emulator)

## iOS
Assurez-vous d'avoir un Macbook, si vous n'en avez pas, achetez-en un, sinon cela ne fonctionnera pas (il n'y a pas de moyen légal d'utiliser iOS sur Windows/Linux).

Après l'installation de xCode, vous obtiendrez la dernière version d'iOS supportée déjà installée.

Vous pouvez utiliser les options suivantes pour démarrer manuellement un simulateur :

- Via l'application Simulator, trouvez-la sur Mac et ajoutez-la à votre dock comme suit

    ![Simulator App](./assets/simualtor-app.jpg)

    ![Simulator start](./assets/start-simulator.jpg)

- Utilisez un module appelé `start-ios-simulator` qui peut être trouvé [ici] (https://github.com/wswebcreation/start-ios-simulator). Avec ce module, vous pouvez facilement utiliser votre terminal pour sélectionner votre simulateur

## Astuce
> Il est conseillé de garder un émulateur en permanence et de démarrer les tests sur un émulateur déjà ouvert pour accélérer les tests.
