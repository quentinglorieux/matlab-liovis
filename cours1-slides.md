---
marp: true
title: "Cours 1 — Introduction à Matlab"
author: "Quentin Glorieux"
paginate: true
theme: default
class: lead
---

# Cours 1.1
## Introduction à Matlab

Bases, scripts, fonctions, graphiques

---

## Objectifs du cours

- Comprendre l’environnement Matlab  
- Manipuler variables, vecteurs, matrices  
- Écrire un premier script  
- Écrire une première fonction  
- Tracer des graphiques 1D  
- Afficher une image simple (préparation traitement d’image)

---

## Matlab : qu’est-ce que c’est ?

Environnement de calcul numérique intégrant :

- Un **interpréteur interactif** (Command Window)  
- Un **langage de programmation** structuré  
- Des **outils graphiques** pour l’analyse et la visualisation  
- De nombreuses **toolbox** (signal, image, optimisation…)

---

## Interface Matlab (1/2)

Éléments principaux :

- **Command Window**  
- **Editor**  
- **Workspace**  
- **Current Folder**  

> Bon réflexe : travailler dans un **dossier dédié**.

---

## Interface Matlab (2/2)

L’Editor permet de créer :

- des **scripts** (`.m`)
- des **fonctions** (`.m`)

Les messages d’erreur Matlab sont généralement très explicites.

---

## Premières variables

```matlab
a = 3;
b = [1 2 3];
M = [1 2; 3 4];
```

---

## Indexation (Matlab commence à 1)

```matlab
M(2,1)      % élément ligne 2, colonne 1
b(3)        % troisième élément
```

---

## Création de vecteurs et matrices

```matlab
z = zeros(3,3);
u = ones(1,10);
x = linspace(0,10,100);
t = 0:0.01:1;
I = eye(4);
```

---

## Opérations essentielles

```matlab
A * B       % multiplication matricielle
A .* B      % produit élément par élément
A'          % transposition
norm(A)     % norme
inv(A)      % inverse (à éviter)
```

---

## Scripts : définition

Un script est un fichier `.m` :
- exécuté de haut en bas  
- partagé avec le Workspace  
- utile pour les enchaînements simples  

---

## Exemple de script

```matlab
% script_test.m
x = 0:0.1:10;
y = sin(x);
plot(x, y);
```

---

## Fonctions : intérêt

Une fonction :
- possède son propre espace de variables  
- n’affecte pas le Workspace  
- structure un projet  

---

## Fonction : structure de base

```matlab
function sortie = carre(x)
    sortie = x.^2;
end
```

---

## Fonction à plusieurs sorties

```matlab
function [moy, ecart] = stats(v)
    moy   = mean(v);
    ecart = std(v);
end
```

---

## Tracer une courbe

```matlab
x = linspace(0,2*pi,200);
plot(x, sin(x));
```

---

## Mise en forme d’une figure

```matlab
plot(x, y, 'LineWidth', 2);
title('Sinus');
xlabel('x');
ylabel('sin(x)');
grid on;
```

---

## Superposition de courbes

```matlab
plot(x, sin(x),'r'); hold on;
plot(x, cos(x),'b');
legend('sin','cos');
```

---

## Subplots

```matlab
subplot(2,1,1); plot(x, sin(x));
subplot(2,1,2); plot(x, cos(x));
```

---

## Afficher une image

```matlab
I = imread('cameraman.tif');
imagesc(I); colormap gray; axis image;
```

---

## Exercice (1/2)

Créer un script `signal1.m` qui génère et trace la somme de deux signaux sinusoïdaux.


---

## Exercice  (2/2)

Créer une fonction `amplitude.m` qui calcule l’amplitude d’un signal.


Utiliser la fonction `amplitude` dans le script `signal1.m` pour afficher l’amplitude du signal.


---

## Zoom temporel
Ajouter dans le script `signal1.m` pour zoomer sur les 50 premiers millisecondes.

---

## Mini-TP : Profil d'image

Créer un script `profil_image.m` qui charge une image, extrait la ligne 100 et trace son profil d’intensité.

---

## Conclusion

Compétences acquises :
- bases de l'interface Matlab  
- scripts et fonctions  
- graph 1D
- affichage d’image  

