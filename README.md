# LAB 22 : Développement Android avec JNI (Java Native Interface)
## Introduction
Dans ce laboratoire, l’objectif est de construire une application Android nommée JNIDemo capable de communiquer avec du code natif C++ via JNI. L’application appellera plusieurs fonctions natives, enverra des paramètres Java vers C++, récupérera des résultats calculés côté natif, et apprendra à gérer correctement le chargement de la bibliothèque partagée .so.
Ce lab permet aussi de comprendre pourquoi JNI est encore utilisé dans les applications modernes : calcul intensif, réutilisation de bibliothèques C/C++, encapsulation d’algorithmes sensibles, traitement temps réel, ou ajout de couches de résistance au reverse engineering. JNI reste une interface “raisonnablement efficace”, mais Android recommande de limiter les allers-retours Java/native et de garder l’API JNI propre et bien organisée.

## objectifs 
À la fin de ce laboratoire, il sera possible de :
créer un projet Android avec support C++ ;
comprendre le rôle du NDK, de CMake et de JNI ;
déclarer et appeler des méthodes natives depuis Java ;
manipuler des types simples et complexes entre Java et C++ ;
gérer des erreurs fréquentes comme UnsatisfiedLinkError ;
lire les logs natifs dans Logcat ;
appliquer de bonnes pratiques récentes pour JNI, optimisation et sécurité.
## Créer le projet Android avec support C++
Ouvrir Android Studio puis suivre :
File → New Project → Empty Views Activity
Configurer ainsi :
Name : JNIDemo
Language : Java
Minimum SDK : API 24
cocher Include C++ support
Build system : CMake
Valider avec Finish.
Ce qu’Android Studio génère automatiquement
Le projet crée en général :
un dossier cpp/
un fichier native-lib.cpp
un fichier CMakeLists.txt
la configuration Gradle pour la compilation native
Android Studio prend officiellement en charge l’ajout de code C/C++ à un projet Android à l’aide du NDK et de CMake.
Point de contrôle
À ce stade, le projet doit se synchroniser sans erreur.
Si Gradle affiche un problème lié au NDK ou à CMake, ouvrir :
Tools → SDK Manager → SDK Tools
et vérifier que :
NDK (Side by side)
CMake
LLDB
sont bien installés.


## Compiler et exécuter
Lancer l’application sur un émulateur ou un téléphone réel.
Résultat attendu :
Hello from C++ via JNI !
Factoriel de 10 = 3628800
Texte inverse : !lufrewop si INJ
Somme du tableau = 150



<img width="333" height="507" alt="Screenshot 2026-03-25 142834" src="https://github.com/user-attachments/assets/19f3c712-b4ba-442a-96a6-f68924baf1d1" />

<img width="1876" height="616" alt="Screenshot 2026-03-25 143259" src="https://github.com/user-attachments/assets/080600fe-4712-4b0b-b6c3-d814482bf30b" />



## Conclusion
JNI est une passerelle puissante entre Java et C++, mais il faut l’utiliser avec méthode. Android le présente comme une solution efficace pour interagir avec du code natif, tout en rappelant qu’il reste plus complexe que le code managé. Le bon usage consiste donc à réserver JNI aux traitements réellement utiles : calcul intensif, bibliothèques natives existantes, logique sensible, ou services bas niveau.
Avec ce laboratoire, l’application JNIDemo devient un excellent point de départ pour des projets plus avancés comme :
chiffrement natif,
détection anti-debug,
traitement d’image avec OpenCV,
IA embarquée,
sécurité applicative Android.
