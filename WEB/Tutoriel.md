# 🌐 TUTORIEL : Web 🌐

## 📜 Énoncé 📜

Voici une page web avec un écran de connexion : [https://cyberini.com/ctfs/assets/tutoweb.php](#). Sauriez-vous trouver le mot de passe pour s'y connecter ? 🤔

## 🔎 Indice 🔎

Les sites web ont toujours un côté "client" visible (le code source) et un côté "serveur" 💻.

## 🔍 Étapes à suivre 🔍

1. **Accéder à la page web** :
   - Ouvrez la page web dans votre navigateur. 🌐

2. **Inspecter le code source** :
   - Faites un clic droit sur la page et sélectionnez "Inspecter" ou "Afficher le code source de la page" (`Ctrl+U`). 🔍

3. **Analyser le code JavaScript** :
   - Recherchez le code JavaScript dans le code source. Vous devriez trouver quelque chose comme ceci :
     ```javascript
     \$("#bouton").on("click", function (event) {
         if (\$("#inputPassword").val() == "flag{CTFWEB}") {
             alert("Bienvenue !");
             \$(".form-signin").html("Connecté avec succès.");
             event.preventDefault();
         }
         else {
             alert("Mauvais mot de passe !!");
             event.preventDefault();
         }
     });
     ```

4. **Trouver le mot de passe** :
   - En examinant le code JavaScript, vous pouvez voir que le mot de passe est `flag{CTFWEB}`. 🔑

5. **Entrer le mot de passe** :
   - Entrez `flag{CTFWEB}` dans le champ de mot de passe de la page web et cliquez sur le bouton de connexion. 🔓

6. **Valider le flag** :
   - Si le mot de passe est correct, vous verrez un message de bienvenue et le formulaire sera mis à jour pour indiquer que vous êtes connecté avec succès. 🎉

## 🏆 Résultat 🏆

En suivant ces étapes, vous devriez être en mesure de trouver le mot de passe et de vous connecter à la page web. Le flag est `flag{CTFWEB}`. 🏁
