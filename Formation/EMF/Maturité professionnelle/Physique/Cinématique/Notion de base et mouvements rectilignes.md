## Définition 

![[Pasted image 20231127161444.png]]

Distance = $d=Δx = x - x_0$
Temps = $t=Δt = t - t_0$

MRU = Mouvement rectiligne uniforme
MRUA = Mouvement rectiligne uniforme accéléré

## Vitesse 
- La vitesse moyenne $v_{moy}$ d'un mobile est la distance $\Delta x$ parcourue divisée par le temps $\Delta t$ : $v_{moy} = \frac{\Delta x}{\Delta t}$.
- La vitesse instantanée est la limite de la vitesse moyenne lorsque $\Delta t$ tend vers zéro.
## L'accélération
- L'accélération $a_{moy}$ est la variation de vitesse $\Delta v$ sur la variation de temps $\Delta t$ : $a_{moy} = \frac{\Delta v}{\Delta t}$.
- C'est une grandeur vectorielle.

## MRU

![[Pasted image 20231127162115.png]]

- Un mobile en MRU se déplace avec une vitesse constante.
- Position $x$ à un instant $t$ : $x = v \cdot (t - t_0) + x_0$ où $v$ est la vitesse constante.


### MRU et vitesse 

![[Pasted image 20231127162332.png]]
- MRUA est caractérisé par une accélération constante.
- Vitesse $v$ à un instant $t$ : $v = a \cdot (t - t_0) + v_0$.
- Position $x$ à un instant $t$ : $x = \frac{1}{2}a \cdot (t - t_0)^2 + v_0 \cdot (t - t_0) + x_0$

Ceci est une [[Fonctions affines|fonction linéaire]] comme $y=ax+b$

## [[Drawing 2023-11-29 12.30.47.excalidraw|Exercice]]

# Cinématique résumé

- Étude du mouvement uniquement
- Ne s’intéresse pas aux causes du mouvement (forces)
- Mouvements rectilignes uniformes (MRU) ou uniformément accélérés (MRUA)
  - horizontaux (axe des x) : p.ex. mobile sur le banc cinématique
  - verticaux (axe des y) : p.ex. chute libre

| grandeur       | définition                    | symbole       | formule           |
| -------------- | ----------------------------- | ------------- | ----------------- |
| instant        | moment précis                 | $t$ [s]       |                   |
| durée          | intervalle entre deux instants| $\Delta t$ [s]| $\Delta t = t - t_0$ |
| position       | endroit précis                | $x$ [m]       |                   |
| distance       | espace entre deux positions   | $d$ [m]       | $d = x - x_0$     |
| vitesse        | distance parcourue sur une durée | $v$ [m/s]  | $v_m = \frac{\Delta x}{\Delta t} = \frac{d}{\Delta t}$ |
| accélération   | variation de la vitesse sur une durée | $a$ [m/s^2] | $a_m = \frac{\Delta v}{\Delta t}$ |

## Formules importantes (mouvements horizontaux) :

Calcul de la vitesse :
$$ v = a \cdot (t - t_0) + v_0 $$

Calcul de la vitesse moyenne :
$$ v_{moy} = \frac{v + v_0}{2} $$

Calcul de la position (1) :
$$ x = v_{moy} \cdot (t - t_0) + x_0 $$

Calcul de la position (2) :
$$ x = \frac{1}{2} \cdot a \cdot (t - t_0)^2 + v_0 \cdot (t - t_0) + x_0 $$

Relation entre $a$, $v$ et $x$ :
$$ v^2 - v_0^2 = 2 \cdot a \cdot (x - x_0) $$

*Remarque* : pour la chute libre (verticale), on remplacera les symboles $x$ par $y$ et $a$ par $-g$. 

[[Drawing 2023-12-20 13.41.07.excalidraw]]