# 🌐 La Source des ennuis 🌐

## 📜 Énoncé 📜

Trouvez le flag à partir de la page web suivante : [La source des ennuis](#).

## 🔍 Indice 🔍

Le code source est toujours une bonne piste pour débuter ! 🔎

## 🔎 Étapes à suivre 🔎

1. **Inspecter le code source** :
   - Ouvrez la page web dans votre navigateur. 🌐
   - Faites un clic droit sur la page et sélectionnez "Inspecter" ou "Afficher le code source de la page" (`Ctrl+U`). 🔍

2. **Analyser le code HTML** :
   - Recherchez le champ email dans le code source. Vous devriez trouver quelque chose comme ceci :
     ```html
     <input type="email" id="inputEmail" name="inputEmail" class="form-control" placeholder="michel@mail.com" required="" autofocus="" disabled="">
     ```
   - Remarquez que le champ email est désactivé (`disabled=""`). 🚫

3. **Modifier le code HTML** :
   - Supprimez l'attribut `disabled` du champ email pour le rendre actif. ✏️

4. **Entrer les informations de connexion** :
   - Entrez `admin@mail.com` comme adresse email. 📧
   - Entrez `pizzaman` comme mot de passe. 🔒
   - Cliquez sur le bouton de connexion. 🔓

5. **Valider le flag** :
   - Après avoir entré les informations de connexion, vous devriez voir le flag `W3bInv3st!gat0r`. 🏆

## 🏁 Résultat 🏁

En suivant ces étapes, vous devriez être en mesure de trouver le flag et de valider le challenge. Le flag est `W3bInv3st!gat0r`. 🏁
