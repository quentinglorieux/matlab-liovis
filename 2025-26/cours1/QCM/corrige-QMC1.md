# QCM corrigé — Cours 1 : Introduction à Matlab

## 1.  
**Un script Matlab est…**  
 Un fichier `.m` exécuté de haut en bas  
**Explication :** un script est une simple liste d’instructions exécutées séquentiellement, sans définition de fonction.

---

## 2.  
**Une fonction Matlab…**  
 Possède son propre espace de variables  
**Explication :** les fonctions ne voient pas les variables du Workspace (sauf globales), ce qui évite les conflits.

---

## 3.  
**Indexation dans Matlab :**  
 à 1  
**Explication :** Matlab hérite du langage Fortran, qui commence l’indexation à 1.

---

## 4.  
`linspace(0,10,100)` génère :  
 un vecteur de 100 valeurs entre 0 et 10  
**Explication :** `linspace(a,b,n)` crée `n` points régulièrement espacés entre `a` et `b`.

---

## 5.  
`zeros(3,2)` crée :  
 une matrice 3×2 de zéros  
**Explication :** la première dimension = lignes, la seconde = colonnes.

---

## 6.  
Multiplication **élément par élément** :  
 `A .* B`  
**Explication :** l’opérateur `.*` applique la multiplication entrée par entrée.

---

## 7.  
`A'` correspond à :  
 la transposée (conjuguée)  
**Explication :** `'` réalise la transposition conjugée pour les complexes (et simple transposition pour les réels).

---

## 8.  
La fonction `carre(x)` doit être dans :  
 `carre.m`  
**Explication :** le nom du fichier doit correspondre au nom de la fonction principale.

---

## 9.  
`plot(x,y)` :  
 Trace une courbe de y en fonction de x  
**Explication :** fonction de base de tracé 2D en Matlab.

---

## 10.  
`hold on` permet de :  
 Ajouter des courbes sur la même figure  
**Explication :** sans `hold on`, chaque nouvel appel à `plot` efface le précédent.

---

## 11.  
`subplot(2,1,1)` :  
 Figure composée de 2 lignes, 1 colonne, zone 1  
**Explication :** `subplot(m,n,p)` → position p dans une grille m×n.

---

## 12.  
`imagesc(I)` :  
 Affiche la matrice comme image  
**Explication :** normalise automatiquement l’échelle des couleurs sur les valeurs présentes.

---

## 13.  
Intérêt principal des fonctions :  
 Réutiliser et structurer du code  
**Explication :** centraliser le calcul, réduire les répétitions, faciliter la maintenance.

---

## 14.  
Activer une grille :  
 `grid on`  
**Explication :** commande standard pour afficher une grille sur le graphique courant.

---

## 15.  
Ajouter un titre :  
 `title()`  
**Explication :** la fonction `title()` ajoute un titre à la figure active.

---

## 16.  
Une variable définie dans un script :  
 reste dans le Workspace  
**Explication :** les scripts partagent leur environnement avec la Command Window.

---

## 17.  
Syntaxe correcte d’une fonction à deux sorties :  
 `function [s1, s2] = f(x)`  
**Explication :** les sorties multiples doivent être entre crochets.

---

## 18.  
Vecteur à pas fixe :  
 `0:0.001:1`  
**Explication :** l’opérateur `:` crée des vecteurs avec un pas constant (ici 0.001).

