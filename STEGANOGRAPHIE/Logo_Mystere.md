
# 🖼️ Challenge : Le logo mystère  

**📜 Nom :** Le logo mystère  
**🕵️ Énoncé :**  
> Je sais pas, mais... ce logo est bizarre. J'ai l'impression qu'il y a quelque chose dedans. Voyez par-vous même.  

**💡 Indice :** Data URL  

---

## 🚀 Résolution  

### 1️⃣ **Téléchargement du fichier**  
J'ai commencé par télécharger le fichier **logo.png** sur ma VM. 🤔

---

### 2️⃣ **Extraction de la chaîne en Base64**  
J'ai utilisé la commande `strings` pour analyser le fichier. Cela m'a permis de découvrir une longue chaîne en Base64 ressemblant à ceci :  
```plaintext
data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAHEAAAARCAMAAADdVLO4AAAAAXNSR...
```

Cette chaîne encode l'image dans le format `data:image/png;base64`. 🧵

---

### 3️⃣ **Décodage de la chaîne Base64**  
Pour extraire l'image, j'ai utilisé la commande suivante :  
```bash
echo "iVBORw0KGgoAAAANSUhEUgAAAHEAAAARCAMAAADdVLO4AAAAAX..." | base64 -d > logo.png
```

---

### 4️⃣ **Ouverture du fichier**  
Après avoir généré le fichier `logo.png`, je l'ai ouvert avec un visualiseur d'images. 👀

---

### 🎉 **Le flag !**  
L'image contenait directement le texte :  
```plaintext
NotHidden
```

---

## 🏁 Flag : **`NotHidden`**

---

## 🔧 Outils utilisés  
- `strings` 🛠️  
- `base64` 📜  
- Un visualiseur d'images 🖼️  

---

🎊 **Challenge terminé avec succès !** 🎊
