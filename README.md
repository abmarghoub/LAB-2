# LAB 2 – Calculateur d’impôts locaux : Saisie, traitement et affichage

---
### Réalisé par

**Abla MARGHOUB**

### Encadré par

**Pr. Mohamed LACHGAR**

### Module

**Techniques de Programmation Avancée**

### Établissement

**École Normale Supérieure - Université Cadi Ayyad**

---


## 1. Objectif du TP
Développer un interface Android permettant de calculer le montant total des impôts locaux en fonction de la surface, du nombre de pièces et de la présence d’une piscine, tout en collectant les informations de l’utilisateur (nom et adresse).

---

## 2. Architecture technique

### 2.1 Stack technique
| Élément | Description |
|----------|-------------|
| **Langage principal** | Java |
| **IDE utilisé** | Android Studio |
| **Version Android minimale (API)** | 24 (Android 7.0 Nougat) |
| **Système de build** | Gradle |
| **Structure du layout** | XML (LinearLayout vertical) |
| **Ressources** | `strings.xml` |
| **Composants UI** | `TextView`, `EditText`, `CheckBox`, `Button` |
| **Gestion des événements** | `setOnClickListener()` |
| **Affichage des messages** | `TextView` pour le résultat |
| **Émulateur utilisé** | Android Virtual Device (AVD) ou smartphone physique |

### 2.2 Structure du code

<img width="457" height="756" alt="11" src="https://github.com/user-attachments/assets/71517071-531b-42a7-abcb-87e98feaa9e8" />

---

## 3. Composants et fonctionnement de l’application

### 3.1 Interface (XML)  
`activity_main.xml` définit la structure de l’écran :  

- Champs de saisie pour **Nom**, **Adresse**, **Surface** et **Nombre de pièces**.  
- **CheckBox** pour indiquer la présence d’une piscine.  
- **Bouton Calculer** pour lancer le calcul des impôts.  
- **TextView Résultat** pour afficher l’impôt de base, le supplément et le total.  
- Utilisation de **LinearLayout vertical** pour un alignement clair et responsive.  
- La Checkbox et le bouton sont placés sur la même ligne avec **weightSum** et **layout_weight** pour une répartition proportionnelle.

### 3.2 Logique (Java)  
`MainActivity.java` contient :  

- Le lien entre l’interface graphique et le code via `findViewById()`.  
- La lecture des valeurs saisies dans les EditText et la CheckBox.  
- Le calcul de l’impôt de base (`surface * 2`), du supplément (`pieces * 50 + 100 si piscine`) et du total.  
- L’affichage du résultat complet dans le `TextView` avec toutes les informations de l’utilisateur (Nom, Adresse, Impôts).  
- La gestion des événements avec `setOnClickListener()` pour le bouton Calculer.  
- La gestion d’erreurs pour éviter les saisies invalides avec `try-catch`.  

### 3.3 Ressources (XML)  
`strings.xml` contient :  

- Tous les textes statiques de l’application (labels, hints, texte du bouton).  
- Les valeurs utilisées dans l’interface pour simplifier la maintenance et la traduction future.  

---

## 4. Résultat attendu

### 4.1 Compilation du projet
Le projet doit se compiler sans erreur sous Android Studio et s’exécuter sur un émulateur ou un appareil Android.  

<img width="952" height="387" alt="12" src="https://github.com/user-attachments/assets/6b6818e5-70a4-4512-a022-a35927313122" />


### 4.2 Interface de l’application

L’application doit présenter un formulaire clair avec tous les champs, la checkbox et le bouton sur la même ligne, et afficher le résultat complet après le calcul.  

<img width="802" height="591" alt="13" src="https://github.com/user-attachments/assets/e896ef32-0aec-47e1-ba64-db243046b60a" />


---

## 5. Démonstration vidéo

https://github.com/user-attachments/assets/2baea879-b11a-46be-ba92-35441d8cd90c


