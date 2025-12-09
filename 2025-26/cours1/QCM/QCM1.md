# QCM — Cours 1 : Introduction à Matlab

## 1.  
Quelle est la structure de base d’un script Matlab ?  
- A : Une fonction avec un retour obligatoire  
- B : Un fichier `.m` exécuté de haut en bas  
- C : Un fichier compilé avant exécution  
- D : Un fichier indépendant du Workspace  

---

## 2.  
Laquelle des propositions décrit correctement une **fonction** Matlab ?  
- A : Elle modifie toujours le Workspace  
- B : Elle possède son propre espace de variables  
- C : Elle ne peut pas avoir de sortie  
- D : Elle ne peut être appelée que dans un script  

---

## 3.  
Dans Matlab, l’indexation commence :  
- A : à 0  
- [ ] à 1  
- [ ] à –1  
- [ ] cela dépend du type de variable  

---

## 4.  
La commande `linspace(0,10,100)` génère :  
- [ ] un vecteur de 100 valeurs espacées d’un pas de 1  
- [ ] un vecteur de 100 valeurs entre 0 et 10  
- [ ] un vecteur de taille 101  
- [ ] une matrice 10×100  

---

## 5.  
Que fait la commande `zeros(3,2)` ?  
- [ ] Crée un vecteur ligne de trois zéros  
- [ ] Crée une matrice 3×2 de zéros  
- [ ] Crée une matrice 2×3 de zéros  
- [ ] Efface trois variables  

---

## 6.  
Laquelle de ces instructions effectue une multiplication **élément par élément** ?  
- [ ] `A * B`  
- [ ] `A .* B`  
- [ ] `A . B`  
- [ ] `A x B`  

---

## 7.  
La commande `A'` correspond à :  
- [ ] l’inverse de A  
- [ ] l’adjointe (transposée conjuguée) de A  
- [ ] la dérivée de A  
- [ ] la symétrisation de A  

---

## 8.  
Quel fichier doit contenir la fonction `carre(x)` ?  
- [ ] `script.m`  
- [ ] `function.m`  
- [ ] `carre.m`  
- [ ] n’importe quel nom  

---

## 9.  
Que fait l’instruction `plot(x,y)` ?  
- [ ] Affiche une image  
- [ ] Trace une courbe de y en fonction de x  
- [ ] Calcule la FFT de y  
- [ ] Enregistre une figure  

---

## 10.  
Que permet `hold on` ?  
- [ ] Remplacer la figure existante  
- [ ] Ajouter des courbes sur la même figure  
- [ ] Effacer la figure  
- [ ] Changer l’échelle des axes  

---

## 11.  
La commande `subplot(2,1,1)` prépare une figure :  
- [ ] composée de 2 lignes et 1 colonne, zone 1  
- [ ] de 1 ligne et 2 colonnes, zone 1  
- [ ] de 2 graphiques superposés non indépendants  
- [ ] de 2 fenêtres séparées  

---

## 12.  
`imagesc(I)` :  
- [ ] efface la matrice  
- [ ] affiche la matrice comme image  
- [ ] convertit la matrice en double  
- [ ] calcule le spectre de l’image  

---

## 13.  
Quel est l’intérêt principal d’une fonction ?  
- [ ] Augmenter la taille du Workspace  
- [ ] Réutiliser et structurer du code  
- [ ] Accéder directement aux variables globales  
- [ ] Modifier automatiquement le dossier courant  

---

## 14.  
Quelle commande active la grille sur une figure ?  
- [ ] `grid on`  
- [ ] `meshgrid`  
- [ ] `show grid`  
- [ ] `enableGrid()`  

---

## 15.  
Quelle commande permet d’ajouter un titre ?  
- [ ] `figtitle`  
- [ ] `title()`  
- [ ] `label()`  
- [ ] `text()`  

---

## 16.  
Une variable définie dans un script :  
- [ ] disparaît immédiatement  
- [ ] reste dans le Workspace  
- [ ] n’est accessible que dans les fonctions  
- [ ] devient automatiquement globale  

---

## 17.  
Syntaxe correcte d’une fonction à deux sorties :  
- [ ] `function sortie1, sortie2 = f(x)`  
- [ ] `function [s1, s2] = f(x)`  
- [ ] `function f(x) = [s1, s2]`  
- [ ] `function {s1, s2} = f(x)`  

---

## 18.  
Quel vecteur a un **pas fixe** ?  
- [ ] `linspace(0,1,1000)`  
- [ ] `0:0.001:1`  
- [ ] `time(0,1,1000)`  
- [ ] `seq(0,1,0.001)`  

---

## 19.  
La commande `imread('cameraman.tif')` :  
- [ ] charge une image dans une matrice  
- [ ] trace automatiquement l’image  
- [ ] calcule la FFT  
- [ ] charge un fichier audio  

---

## 20.  
`max(abs(v))` retourne :  
- [ ] l’indice du maximum  
- [ ] la plus grande valeur absolue  
- [ ] la moyenne  
- [ ] la norme euclidienne  