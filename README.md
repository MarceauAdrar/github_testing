# Procédure

## Étape 1:
Vous allez partir sur un projet tout neuf pour vous entrainer.
Pour nous faciliter encore un peu plus la vie, nous allons utiliser un script qui va nous permettre de personnaliser nos divers éléments (nom de projet, variables d'environnements, ...).

1. Téléchargez le contenu de ce *repository* à l'aide de la commande `git clone https://github.com/MarceauAdrar/github_testing master` si le projet n'existe pas, sinon `git pull https://github.com/MarceauAdrar/github_testing master` si vous l'aviez déjà téléchargé auparavant (pour les appareils moins tolérants ou ne prenant pas en charge le sh, vous pouvez télécharger le contenu sur la branche `base` avec la commande `git clone https://github.com/MarceauAdrar/github_testing base`.
2. Déplacez le fichier `script.sh` dans le dossier *www* de Wamp ou *htdocs* de XAMPP.
3. Ouvrez un terminal de commande à l'endroit où se trouve ce fichier et tapez la commande suivante: `sh script.sh`
   - Cette commande va lancer le script !
   - Vous devriez avoir ceci:<br>
     ![image](https://github.com/user-attachments/assets/439cf872-f61d-4881-9706-b8c92ba2d1e0)
   - Saisissez les informations demandées (**sans espace**, **ni accent**) nom de votre projet, nom de la BDD, utilisateur BDD, MDP utilisateur BDD, l'hôte (devrait être: localhost), le chemin **complet** de votre dossier (une erreur peut apparaitre, vérifiez si le dossier s'est créé.
   - Une fois le projet ouvert dans VScode, vous devriez avoir quelque chose de semblable à ceci:<br>
     ![image](https://github.com/user-attachments/assets/b12a3b2d-554c-42df-bde9-c3f21d83c05f)

## Étape 2: ([`télécharger`](<https://github.com/MarceauAdrar/github_testing/tree/step02>))
Vous allez mainteant devoir télécharger et installer notre dépendance `Cypress` qui va nous servir de librairie de tests.

Tapez la commande suivante: `npm init -y`: cela va initialiser un repository pour gérer les dépendances (un peu comme composer), un fichier `package.json` va être créé à la racine du projet.
Ensuite, tapez ceci: `npm install -D cypress`
Une fois la dépendance installée, vous devriez avoir ce contenu dans le fichier<br>
![image](https://github.com/user-attachments/assets/37212109-a758-4d37-a42e-8ab18dc6574b)<br>
Changez le contenu de la clé "test" dans "scripts" vers ceci:<br>
![image](https://github.com/user-attachments/assets/26c9aae7-524a-4847-945f-0aa8c8e352e3)

## Étape 3: ([`Lancer un test`](<https://github.com/MarceauAdrar/github_testing/tree/step03>))
Maintenant que toutes nos bibliothèques sont installées, nous pouvons lancer d'autres commandes !
Tapez `npm run test`: cette commande lance la commande sous l'*alias* "test" dans les "scripts" de notre fichier `package.json`.
Vous devriez avoir:
- la console qui est occupée et retourne les logs ![image](https://github.com/user-attachments/assets/081f7fd7-4f57-4751-aada-2ef0d3740b02)
- une fenêtre Cypress qui apparaît ![image](https://github.com/user-attachments/assets/91ade535-ce77-4734-986d-c5ee7cbab79b)

Nous allons maintenant générer notre premier test:
1. Cliquez sur E2E Testing<br>
![image](https://github.com/user-attachments/assets/a7aef1d2-9244-4efe-af46-94d0f2feae2b)
2. Cliquez sur "Continue"
3. Lancez le test avec un navigateur (ex. Chrome)
4. Une nouvelle fenêtre "contrôlée" vient s'ouvrir<br>
![image](https://github.com/user-attachments/assets/dbbe19cf-b3a0-49b6-9943-3139aadced11)
5. Cliquez sur "Create new spec"<br>
![image](https://github.com/user-attachments/assets/b2815bb8-604d-4b56-9414-3b41b41e311d)
6. Donnez lui un nom (**ne changez pas le chemin**), ici nous allons l'appeler `spec.cy.js`<br>
![image](https://github.com/user-attachments/assets/007d1f9b-f891-414f-b2bb-d672eb18b3b5)<br>
et hop ! Notre test (très basique) a été généré, nous pouvons maintenant le personnaliser sur l'interface proposée, ou directement depuis VScode en ouvrant le fichier `cypress\e2e\spec.cy.js` !<br>
![image](https://github.com/user-attachments/assets/1b680771-a402-46a0-b285-03ed36d13280)<br>

Lancez le test et regardez ce qu'il se passe !

## Étape 4: ([`Créer un test E2E`](<https://github.com/MarceauAdrar/github_testing/tree/step04>))
⚠️ Pensez à adapter le projet pour que la suite soit fonctionnelle ! ⚠️
Ajoutez des objets et une connexion à la BDD<br>
Ci-contre, le MCD:<br>
![image](https://github.com/user-attachments/assets/0e78c880-4067-44c2-b02e-ae0fd6032021)
