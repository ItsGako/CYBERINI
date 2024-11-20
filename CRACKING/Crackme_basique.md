# Crack Me Basique 🕵️‍♂️🔐

## Description du Challenge 🎮
Le but de ce challenge était de retrouver le mot de passe du "Crack Me" à partir d'un fichier exécutable. Cependant, lorsqu'on essaie d'ouvrir le fichier, on obtient un message d'erreur. 🤔 Le challenge consiste donc à contourner cette erreur pour récupérer le mot de passe.

### Indices 🔍
- **Indice 1** : "/stɹɪŋ/" 🔑  
Cela nous indique d'utiliser la commande `strings`, qui permet d'extraire les chaînes de caractères lisibles d'un fichier binaire. C'est une piste pour trouver le mot de passe caché !

- **Indice 2** : "\de.bœ.ɡe\" 💬  
Cela ressemble à une chaîne phonétique ou une référence à une opération sur le fichier binaire. Mais nous allons d'abord utiliser `strings` pour voir si cela nous donne quelque chose de plus direct.

## Étapes de Résolution 🛠️

1. **Téléchargement du fichier** 🖥️
   - Tout d'abord, j'ai récupéré le fichier à l'aide de la commande `wget` :
     ```bash
     wget https://cyberini.com/ctfs/assets/crackme-linux.exe
     ```

2. **Vérification du type du fichier** 🔍
   - Ensuite, j'ai vérifié le type du fichier téléchargé avec la commande `file`. Cela m'a révélé qu'il s'agissait d'un fichier exécutable au format **ELF 64 bits** :
     ```bash
     file crackme-linux.exe
     # Output: ELF 64-bit LSB executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, not stripped
     ```

3. **Extraction des chaînes avec `strings`** 🧩
   - J'ai utilisé la commande `strings` pour extraire les chaînes de caractères du fichier exécutable. Et là, surprise ! J'ai trouvé un mot de passe directement dans les résultats :
     ```bash
     strings crackme-linux.exe
     # Output:
     # password: 08042023
     ```
   - **Mot de passe trouvé : `08042023`** 🎉

## Conclusion 🏁
Le mot de passe du "Crack Me" était bien **08042023**, et il a été récupéré en utilisant la commande `strings` pour extraire les chaînes de caractères de l'exécutable ELF. 💻🔑

Le challenge est désormais terminé, et la réponse est obtenue ! ✅

### Flag : **CTF{08042023}** 🎯
