# LAB 22 — Développement Android avec JNI (Java Native Interface)

## Introduction

Ce laboratoire consiste à développer une application Android appelée **JNIDemo** capable de communiquer avec du code natif en **C++** via **JNI (Java Native Interface)**.

L’application permettra :

* d’appeler des fonctions natives depuis Java
* d’envoyer des paramètres vers C++
* de récupérer des résultats calculés côté natif
* de gérer correctement le chargement de la bibliothèque `.so`

JNI est utilisé dans plusieurs cas :

* calcul intensif
* réutilisation de bibliothèques C/C++
* protection d’algorithmes sensibles
* traitement en temps réel
* réduction du reverse engineering

> ⚠️ Bonne pratique : limiter les échanges Java ↔ C++ et garder une API JNI propre.

---

## Objectifs

À la fin de ce laboratoire, vous serez capable de :

* créer un projet Android avec support C++
* comprendre le rôle du **NDK**, **CMake** et **JNI**
* déclarer et appeler des méthodes natives
* échanger des données entre Java et C++
* gérer les erreurs (ex : `UnsatisfiedLinkError`)
* lire les logs natifs dans Logcat
* appliquer des bonnes pratiques de performance et sécurité

---

## Création du projet

### Étapes

1. Ouvrir **Android Studio**

2. Aller dans :
   `File → New Project → Empty Views Activity`

3. Configurer :

* **Nom** : JNIDemo
* **Langage** : Java
* **Minimum SDK** : API 24
* ✅ Cocher : Include C++ support
* **Build system** : CMake

4. Cliquer sur **Finish**

---

## Structure générée

Android Studio crée automatiquement :

```text
cpp/
 ├── native-lib.cpp
 └── CMakeLists.txt
```

Avec :

* configuration Gradle native
* intégration NDK

---

## Vérification de l’environnement

Si erreur Gradle :

Aller dans :

```
Tools → SDK Manager → SDK Tools
```

Vérifier :

* NDK (Side by side)
* CMake
* LLDB

---

## Compilation et exécution

Lancer l’application sur :

* un émulateur
* ou un téléphone

---

## Résultat attendu

```
Hello from C++ via JNI !
Factoriel de 10 = 3628800
Texte inverse : !lufrewop si INJ
Somme du tableau = 150
```

---

## Conclusion

Ce laboratoire permet de comprendre :

* l’intégration du code natif en Android
* la communication Java ↔ C++
* l’optimisation des performances
* les bonnes pratiques JNI

---

## Auteur

Projet réalisé dans le cadre du **LAB 22 — JNI Android**.





<img width="333" height="507" alt="Screenshot 2026-03-25 142834" src="https://github.com/user-attachments/assets/4c18566f-4b91-4b3e-94da-645c46e22e07" />



<img width="1876" height="616" alt="Screenshot 2026-03-25 143259" src="https://github.com/user-attachments/assets/531d7af4-77ad-4df3-a9a7-b863d242dd99" />


