# 🔍 TUTORIEL : Inforensique

## 📜 Enoncé

Sauriez-vous trouver quel logiciel a été utilisé pour l'éditer ? (il n'est pas nécessaire de donner la version complète)

## 🔎 Indice

Les photos ont des métadonnées.

## 📸 Étapes à suivre

1. **Télécharger la photo** :
   - Nous avons accès à une photo. Nous la téléchargeons.

2. **Utiliser la commande `file` en bash** :
   - En bash, nous exécutons la commande suivante pour lire les métadonnées de la photo :
     ```sh
     file inforensique.jpg
     ```

3. **Lire les métadonnées** :
   - En examinant les métadonnées, nous voyons la ligne suivante :
     ```
     software=paint.net 5.0.6
     ```

4. **Valider le flag** : 🏆
   - Nous pouvons valider le flag en entrant :
     ```
     paint.net
     ```

