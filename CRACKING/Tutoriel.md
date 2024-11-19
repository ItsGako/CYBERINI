
# 🛠️ TUTORIEL : Cracking 🛠️

## 📄 Énoncé
Voici un script Python. Votre objectif est de retrouver le mot de passe (**flag**) demandé par celui-ci.

### 🧩 Indice
- Explorer le **code source**.
- Décoder un message.

---

## 🚀 Solution pas à pas

### 📜 Le code fourni
```python
# "le code secret est cachÃ©, personnne ne peut le dÃ©chiffrer"
code_secret = "plorevav{synt}"

# correspondance de rÃ©fÃ©rence pour le codage/dÃ©codage
alphabet = str.maketrans('ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz',
   'NOPQRSTUVWXYZABCDEFGHIJKLMnopqrstuvwxyzabcdefghijklm')

def decode_secret(secret):
	# Fonction de dÃ©codage ROT13
	return secret.translate(alphabet)


def login():
	# Fonction de connexion au programme

	nom = input("Nom d'utilisateur : ")
	mdp = input("Mot de passe : ")

	if nom == "Michel":
		if mdp == decode_secret(code_secret):
			print("ConnectÃ© avec succÃ¨s !")
		else :
			print("Mot de passe invalide.")
	else :
		print("Nom d'utilisateur invalide.")

login()
```

---

### 🧐 Analyse
1. **Le mot de passe (flag) est dans la variable `code_secret`** :
   ```python
   code_secret = "plorevav{synt}"
   ```

2. Ce mot de passe est chiffré avec un **chiffrement ROT13** :
   - Le script utilise la fonction `str.maketrans` pour créer un alphabet décalé de 13 positions.
   - La fonction `decode_secret()` applique ce décalage pour **décoder**.

3. **Le nom d'utilisateur attendu est** :
   ```python
   nom == "Michel"
   ```

---

### 🛠️ Décodage
- Pour décoder la chaîne `"plorevav{synt}"`, nous utilisons un outil en ligne comme [dCode ROT13](https://www.dcode.fr/chiffre-rot13) 🔑.
- Après avoir décodé, on obtient :
  ```plaintext
  cyberini{flag}
  ```

---

### 🎉 Flag final
Le flag est **`cyberini{flag}`** ! 🏆

---

## ⚙️ Outils utilisés
- Python 🐍
- [dCode ROT13](https://www.dcode.fr/chiffre-rot13) 🔓

---

### 🚩 **Flag : `cyberini{flag}`**
