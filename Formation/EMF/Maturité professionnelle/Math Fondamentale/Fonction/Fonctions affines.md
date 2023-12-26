## 8.1 Droite et fonction affine

#### 8.1.1 Fonction affine

On appelle **fonction affine**, une fonction définie par : $f(x) = ax + b$ où les nombres $a$ et $b$ sont des réels quelconques.

- Une fonction affine est représentée par une droite (appelée aussi courbe représentative), où $a$ exprime la pente (ou coefficient directeur) et $b$ l'ordonnée à l'origine.

![[Pasted image 20231116114416.png]]
##### Cas particuliers :
- Une fonction affine dont la pente $a$ est nulle est appelée **fonction linéaire**.
- Une fonction affine où $a > 0$ est une fonction **croissante**, et si $a < 0$, elle est **décroissante**.

En principe on parle d'équation d'une droite lorsqu'elle s'écrit sous sa forme cartésienne ou linéaire : $ax + by = c$ ou encore $y = ax + b$ et de fonction affine lorsque la droite est représentée par une fonction $f(x) = ax + b$.

Ainsi, $x = 3$ représente l'équation d'une droite verticale passant par le point (3,0) alors que cette droite ne peut s'exprimer sous la forme d'une fonction de $x$.

### 8.1.2 Pente d'une droite

La pente d'une droite définie par $y = ax + b$ est le rapport $\frac{\Delta y}{\Delta x}$ où $\Delta x$ est l'accroissement selon l'axe des x et $\Delta y$ l'accroissement selon l'axe des y.

Pour calculer la pente d'une droite, on choisit deux points arbitraires $(x_1, y_1)$ et $(x_2, y_2)$, et on utilise la formule :

$$
\text{Pente : } a = \frac{\Delta y}{\Delta x} = \frac{y_2 - y_1}{x_2 - x_1}
$$


![[Pasted image 20231117112329.png]]
#### Exemple 8.2

Calcul de la pente de la droite représentée par le graphe ci-après :

- Le point A a comme coordonnées $(0; 3)$ et le point B les coordonnées $(2; 1)$.
- Ainsi, la pente est calculée comme suit : $a = \frac{1 - 3}{2 - 0} = \frac{-2}{2} = -1$.

### [[Drawing 2023-11-17 10.32.40.excalidraw|Exercice]]
####  Les pentes
![[Pasted image 20231117111710.png]]

## Déterminer l’expression fonctionnelle d’une droite passant par deux points

Donnée : deux points A($x_A$, $y_A$) et B($x_B$, $y_B$)

Chercher : fonctionnelle de la droite… f(x) = $ax +b$ où a et b sont à trouver

### Méthode 1

 1. Calculer la pente 

$a=Δy/Δx$ $=y_{B} - y_{A}/ x_{B} - x_{A}$

2. Ou a donc $f(x) = ax+b$
		Point B: $f(3) === 5$                  (On évalue la fonction en x === 3)
		$4/7 · 3 + b = 5$
		$b = 5-12 /7 = 35-12 /7 = 23/7$

3. Conclure
	Donc $f(x)= 4/7 x + 23/7$

	Remarques :
		- $a = y_{A} - y_{B} / x_{A} - x_{B} = 1-5 / -4 -3 = -4/-7 = 4/7$
		- Point A: $f(-4) === 1$
			$4/7(-4)+b=1$
			$b= 1+ 16/7 = 7+16 /7 = 23/7$

### Méthode 2
Les points A et B sont sur la droite, leurs coordonnées satisfont donc l’[[Équation linéaires|équation]] $y=ax+b$.
$$f(x_{A}) = y_{A}$$
$$f(x_{B}) = y_{B}$$
Exemple :

(1) $$ a(-4) + b = 1 $$ 
(2) $$a · 3 + b = 5 $$
(2) - (1) ==> $7a = 4$
						$a = 4/7$

Puis remplacer $a=4/7$ dans (1) :

$$4/7(-4) + b = 1$$
$$b=23/7$$

[[Drawing 2023-11-20 08.43.15.excalidraw|Exercice]]



## Inverse et opposé
Si deux droites sont perpendiculaires alors leurs pentes sont inverser et opposées
![[Pasted image 20231120103851.png]]

[[Drawing 2023-11-20 10.42.41.excalidraw]]

## Intersection de deux droites
Tous les points de la droite $y=a_{1}x +b_1$  satisfait cette équation. Tous les points de la droite $y=a_{2}x + b_2$ satisfait cette équation-là.

Les points d’intersections de deux droites satisfait donc le système :
$$y=a_{1}x + b_1$$
$$y=a_{2}x + b_2$$

[[Drawing 2023-11-21 08.17.37.excalidraw|Il y a trois cas :]]
### Droite sécantes
![[Pasted image 20231121082447.png]]
### Droite parallèle
![[Pasted image 20231121082509.png]]

### Droites confondues
**![[Pasted image 20231121082625.png]]

