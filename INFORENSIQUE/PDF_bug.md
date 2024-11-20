
# 🕵️‍♂️ Write-up : Un PDF qui bug 📄🔍

## Contexte du Challenge 🚀
Le challenge "Un PDF qui bug" nous demande d'analyser un fichier PDF qui semble corrompu ou dont le type est incorrect. Le défi consiste à déterminer si ce fichier est vraiment un PDF et à trouver le flag caché à l'intérieur. Le message d'erreur indique : "Nous ne pouvons pas ouvrir ce fichier" et l'indice est : **"c'est vraiment un PDF au moins ?"** 🤔

## Étapes de l'analyse 🔍

### 1. Récupération du fichier avec `wget` 🌐
Tout d'abord, j'ai téléchargé le fichier à partir de l'URL fournie en utilisant la commande `wget` :
```bash
wget https://cyberini.com/ctfs/assets/Mon_Document.pdf
```
Le fichier a été téléchargé sous le nom **Mon_Document.pdf**.

### 2. Vérification du type de fichier avec `file` 🧐
Ensuite, j'ai utilisé la commande `file` pour vérifier de quel type de fichier il s'agissait :
```bash
file Mon_Document.pdf
```
Résultat : **Mon_Document.pdf** n'était pas un fichier PDF mais plutôt une **image PNG**. 😲

### 3. Ouverture de l'image 🖼️
J'ai ensuite ouvert l'image téléchargée depuis mes répertoires de téléchargement sur ma machine virtuelle. En examinant l'image, j'ai pu voir qu'il y avait un **flag** bien visible au centre de l'image ! 🎯

Le flag était : 
```
flag:{Easy_Cheesy}
```
🍰

### 4. Conclusion 🎉
Le fichier n'était pas un vrai PDF, mais un fichier PNG déguisé en PDF. Une fois ouvert comme une image, j'ai trouvé le flag en plein milieu. 🎉

**Flag :** `Easy_Cheesy` 😎🍕

## Validation ✅
Le challenge est terminé, le flag a été trouvé et validé avec succès ! 💪

---
C'était un challenge super sympa de forensic 🕵️‍♀️, n'oubliez pas de vérifier le type des fichiers avant de les ouvrir, surtout si quelque chose semble bizarre ! 😊
