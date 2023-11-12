### 1. Définitions et exemples

#### Définition 1.1
Une **équation rationnelle** en x est une [[Équation linéaires|équation]] où la variable x apparaît au moins une fois dans le dénominateur d'une fraction rationnelle et peut être ramenée à une équation polynomiale.

#### Exemple 1.2
Équations rationnelles en x :
- $\frac{3}{x} = \frac{5}{x^2 - x} + \frac{2}{x - 1}$
- $\frac{x^2 + 1}{x + 1} = \frac{5}{x^2 - 1}$

### Méthode de résolution
1. Factoriser tous les dénominateurs présents dans l'équation.
2. Déterminer le domaine de définition de l'équation.
3. Multiplier les deux membres de l'équation par le PPCM des dénominateurs.
4. Résoudre l'équation obtenue après élimination des dénominateurs.
5. Vérifier si les candidats sont dans le domaine de définition et rejeter les solutions étrangères.
6. Écrire l'ensemble des solutions retenues.

**Remarque :** En multipliant par le PPCM, on peut introduire des solutions étrangères non valides, donc cette étape n'établit pas une relation d'équivalence.

### Attention
- Lors de la multiplication par le PPCM, il faut s'assurer de ne pas introduire des solutions étrangères qui ne sont pas dans le domaine de définition de l'équation originale.

## Exemple 1.3 - Résolution d'une équation rationnelle

### Équation donnée
- $\frac{2}{x^2 - 10x + 24} = \frac{1}{4 - x} - \frac{1}{x^2 - 6x}$

### Méthode de résolution
1. Factorisation des dénominateurs :
   - $x^2 - 10x + 24 = (x - 4)(x - 6)$
   - $4 - x = -(x - 4)$
   - $x^2 - 6x = x(x - 6)$

2. [[Domaine de définition d’une équation|Domaine de définition]] (D) :
   - $D = \mathbb{R} \setminus \{0; 4; 6\}$

3. Multiplication des deux membres par le PPCM des dénominateurs :
   - $2x = -1(x - 6) + 4$

4. Réduction et résolution de l'équation polynomiale :
   - $2x = -x^2 + 6x + 4$
   - $x^2 + 3x - 4 = 0$

5. [[Factoriser des expressions algébriques|Factorisation]] et solutions de l'équation :
   - $(x - 1)(x + 4) = 0$
   - Solutions : $x_1 = 1$, $x_2 = -4$

6. Ensemble des solutions retenues :
   - $S = \{1\}$ (car $-4$ n'est pas dans le domaine de définition)

## Remarques sur la Résolution d'Équations Rationnelles

### Remarque 1.4
Les équations rationnelles résolues en Math BF peuvent toutes être ramenées à une équation du 1er ou 2e degré. Il est difficile de prévoir à quel type d'équation polynomiale elles peuvent être ramenées.

### Remarque 1.5
Deux méthodes principales pour résoudre une équation rationnelle :
1. **Laisser les fractions rationnelles** :
   - Garder les fractions dans les deux membres et supprimer les dénominateurs.
   
2. **Rassembler les fractions rationnelles** :
   - Rassembler les fractions dans un des deux membres de l'équation et conserver les dénominateurs.

La première méthode est présentée pour sa simplicité. Pour les inéquations rationnelles, l'utilisation de la seconde méthode sera nécessaire.
## série d’exercices 
[[Drawing 2023-11-08 16.30.10.excalidraw]]