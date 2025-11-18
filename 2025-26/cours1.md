# Cours 1 — Introduction à Matlab : bases, scripts, fonctions, graphiques

## 1. Introduction au fonctionnement de Matlab

Matlab est un environnement de calcul numérique. Il combine :
- un interpréteur interactif (Command Window),
- un langage de programmation structuré,
- un environnement graphique pour l’analyse et la visualisation.

### 1.1. Interface

Points essentiels à trouver :
- Command Window : exécution immédiate de commandes.
- Editor : rédaction de scripts (.m) et fonctions.
- Workspace : variables en mémoire.
- Current Folder : gestion des fichiers.

Important: l’utilisation du dossier courant et sur les messages d’erreur Matlab, qui sont en général explicites.

---

## 2. Manipulation des variables et des matrices

### 2.1. Types de base

Matlab utilise des tableaux numériques comme structure fondamentale.

Exemples :

```matlab
a = 3;
b = [1 2 3];
M = [1 2; 3 4];
```

### 2.2. Indexation

Matlab indexe à partir de 1.

```matlab
M(2,1)      % élément ligne 2 colonne 1
b(3)        % 3ème élément du vecteur
```

### 2.3. Créations utiles

```matlab
z = zeros(3,3);
u = ones(1,10);
x = linspace(0,10,100);
t = 0:0.01:1;      % vecteur temps
I = eye(4);        % matrice identité
```

### 2.4. Opérations essentielles

```matlab
A * B       % multiplication matricielle
A .* B      % multiplication élément par élément
A'          % transposition
inv(A)      % inverse (à éviter dans les systèmes linéaires)
norm(A)     % norme
```

---

## 3. Scripts vs Fonctions : bases indispensables

### 3.1. Script

Un script est une suite d’instructions exécutées de haut en bas. Il utilise et modifie le Workspace. C’est idéal pour des calculs simples ou des tests rapides.

Exemple minimal :

```matlab
% script_test.m
x = 0:0.1:10;
y = sin(x);
plot(x,y);
```

### 3.2. Fonction

Une fonction crée son propre espace de variables (important pour éviter les conflits).  
Syntaxe générale :

```matlab
function sortie = nom_fonction(entree)
    % Commentaire expliquant la fonction
    sortie = entree.^2;
end
```

À enregistrer dans un fichier nom_fonction.m.

### 3.3. Plusieurs sorties

```matlab
function [moy, ecart] = stats(v)
    moy = mean(v);
    ecart = std(v);
end
```

### 3.4. Importance

Important :  
Tout projet Matlab doit être organisé en fonctions.  
Vous devrez rédiger des fonctions au S2 pour le traitement d’image.

---

## 4. Graphiques de base

L’objectif est de tracer et mettre en forme une figure.

### 4.1. Tracer une courbe

```matlab
x = linspace(0, 2*pi, 200);
y = sin(x);
plot(x,y);
```

### 4.2. Ajouter des titres, axes, légendes

```matlab
plot(x, y, 'LineWidth', 2);
title('Sinus');
xlabel('x');
ylabel('sin(x)');
grid on;
```

### 4.3. Plusieurs courbes

```matlab
plot(x, sin(x), 'r'); hold on;
plot(x, cos(x), 'b');
legend('sin','cos');
```

### 4.4. Subplots

```matlab
subplot(2,1,1); plot(x,sin(x));
subplot(2,1,2); plot(x,cos(x));
```

### 4.5. Affichage d’une image

On a besoin d'afficher des images (FFT 2D et traitement d’image) :

```matlab
I = imread('cameraman.tif');
imagesc(I); colormap gray; axis image;
```

---

## 5. Exercice guidé

Objectif : Manipuler les concepts essentiels du cours 1.

Exercice : tracer un signal temporel et créer une fonction associée  
1. Créer un script signal1.m :  
- définir un vecteur temps $t = 0:0.001:1$;  
- construire un signal $s = 2*sin(2*\pi*50*t) + 0.5*cos(2*\pi*120*t)$;  
- afficher ce signal (plot + titres/étiquettes).  
2. Créer une fonction amplitude.m qui renvoie l’amplitude max d’un vecteur :

```matlab
function A = amplitude(v)
    A = max(abs(v));
end
```

3. L’appeler dans le script et afficher l’amplitude :

```matlab
A = amplitude(s);
fprintf('Amplitude du signal : %.2f\n', A);
```

4. Ajouter une seconde figure avec un zoom temporel :

```matlab
figure;
plot(t, s); xlim([0 0.05]);
```

A retenir : scripts, fonctions, graphes, bonnes pratiques de nommage.

---

## 6. Mini-TP

A faire :  
- charger une image,  
- extraire un profil ligne/colonne,  
- tracer le profil,  
- écrire une fonction profil.m qui renvoie le vecteur du profil.


---

## 7. Conclusion du Cours

Vous devez avoir acquis :  
- la manipulation des matrices,  
- l’écriture de scripts et fonctions simples,  
- les bases de la représentation graphique 1D/2D,  
- les premiers réflexes de mise en forme.

