## Définition : population et variable
### Qu’elle est la population de ces données ? Est-ce la pour toutes la variables (= les caractères)
C’est des élèves masculin de la classe 412

### Quelles sont les variables statistiques ?
Âge, taille, pointure, tour du poignet, tour du cou, taille de l’index (valeur numéral)

### Quelles sont les variables qualitatives ?
Couleur des cheveux, couleur des yeux

### Quelles sont les variables qualitatives ordinales ?
Tailles des T-shirts

### Quelles sont les variables quantitatives ?
Âge, taille t-shirt, pointure, poignet, cou, index

### Quelles sont les variables quantitatives discrètes ?
Âge, taille t-shirt

## Quelles sont les variables quantitatives continues ?
Taille, pointure, poignet, cou, index

## Analyse statistique (âge / taille index droit)
### Âge 
- Min : 18
- Max : 24
- Moyenne : 21
- Médiane : 21
- 1er quartiles : $\frac{1}{4}23 = 17.25 => 20$  
- 3eme quartiles : $\frac{3}{4}23 = 5.75 => 21.75$
- Mode : 20
- Étendu : 20
- Écart semi-interquartile : 11
- Variance : 2.6
- Ecart-type : 1.61
- Coefficient de variation : 0.076

```dataviewjs
let path = app.vault.adapter.basePath;
var d3 = require(path+"\\utils\\d3.v7.min.js");

var data = [
  {
    y: [18, 19, 19, 19, 20, 20, 20, 20, 20, 20, 20, 21, 21, 21, 21, 21, 22, 22, 23, 23, 24, 24],
    boxpoints: 'all',
    jitter: 0.3,
    pointpos: -1.8,
    type: 'box'
  }
];

var layout = {};
var config = {};

window.renderPlotly(this.container, data, layout, config)
```

### Taille index
- Min : 8.5
- Max : 11
- Moyenne : 10
- Médiane : 9.5
- 1er quartiles : $\frac{1}{4}23 = 5.75 => 9.5$ 
- 3eme quartiles : $\frac{3}{4}23 = 5.75 => 10$
- Mode : 9.5
- Écart semi-interquartile: 11
- Variance : 0.4
- Equart-type: 0.63
- Coefficient de variation : 0.063

```dataviewjs
let path = app.vault.adapter.basePath;
var d3 = require(path+"\\utils\\d3.v7.min.js");

var data = [
  {
    y: [8.5, 9, 9, 9, 9.5, 9.5, 9.5, 9.5, 9.5, 9.5, 9.5, 9.5, 9.5, 9.5, 9.5, 9.5, 10, 10, 10, 10, 10, 10.5, 10.5, 11],
    boxpoints: 'all',
    jitter: 0.3,
    pointpos: -1.8,
    type: 'box'
  }
];

var layout = {};
var config = {};

window.renderPlotly(this.container, data, layout, config)
```

## Comment trouver :
### Moyenne :
$$\sum\limits \frac{x_{N}}{N}$$
### 1er quartile
$$ \frac{1}{4}N $$
### 3ème quartile
$$\frac{3}{4}N$$
### Mode
En [statistique](https://fr.wikipedia.org/wiki/Statistique "Statistique"), le **mode**, ou **valeur dominante**, est la valeur la plus représentée d'une variable quelconque dans une population donnée. Une répartition peut être unimodale ou [plurimodale](https://fr.wikipedia.org/wiki/Distribution_multimodale "Distribution multimodale") (bimodale, trimodale…), si deux ou plusieurs valeurs de la variable considérée émergent également, voire sans aucun mode (distribution uniforme) si toutes les valeurs de la variable considérée émergent également.


### Écart semi-interquartile
$${1erQuartile}-{3erQuartile}$$
### Variance
$$ \sum\limits \frac{(x_{n}-x_{moyen})^2}{N}= σ^2$$
### Écart type 
$$ σ = \sqrt{σ}$$