# Trier - `sort`

Dans ce chapitre nous allons découvrir quelques algorithmes de tri. 
Pouvoir trier les éléments d'une liste est une fonctionnalité fondamentale dans l'informatique. Le succès énorme de Google est basé sur un tri efficace de l'information, car dans une liste triée on peux trouver un élément **beaucoup** plus vite.

- la fonction `min(liste)` retourne le minimum
- la fonction `max(liste)` retourne le maximum
- la méthode `liste.sort()` trie une liste

## Fonction `min` et `max`

Les fonctions `min()` et `max()` retournent le minimum et le maximum d'une liste à l'aide d'un algorithme.  
Mais comment fonctionne cet algorithme ?

```{codeplay}
liste = [3, 4, 1, 2, 6, 5]

print(min(liste))
print(max(liste))
```

**Exercice** : Modifiez la liste avec des nouvelles valeurs et essayez de nouveau.

## Trouver le minimum

Pour trouver le minimum dans une liste il faut :

- prendre la première valeur comme minimum courant,
- parcourir le reste de la liste,
- garder la valeur comme nouveau minimum si elle est plus petite.

```{codeplay}
liste = [3, 4, 1, 2, 6, 5]

min = liste[0]
for val in liste[1:]:
    if val < min:
        min = val
        
print(min)
```

**Exercice** : Modifiez l'algorithme pour trouver le maximum.

## Créer une liste

Pour visualiser les algorithmes que nous allons rencontrer dans ce chapitre,
nous allons créer des listes avec des nombres aléatoires.

Avec une compréhension nous allons créer :

- une liste `x` avec des valeurs équidistantes dans l'intervalle [-300, 300]
- une liste `y` avec des valeurs aléatoires dans l'intervalle [-200, 200]

```{codeplay}
from random import *

n = 10
d = 600//n
x0 = 300 - d//2
y0 = 200 - d//2
x = [-x0 + i * d for i in range(n)]
y = [randint(-y0, y0) for i in range(n)]

print('x =', x)
print('y =', y)
```

**Exercice** : Modifiez `n` à 14.

## Visualiser une liste

Nous utilisons les listes `x` et `y` pour afficher des points et visualiser la liste `y`.

```{codeplay}
from turtle import *
from random import *

color('blue')
speed(0)
up()

def create(size, bg='skyblue'):
    global n, d, x, y
    getscreen().bgcolor(bg)
    n = size
    d = 600/n
    x0 = 300 - d//2
    y0 = 200 - d//2
    x = [-x0 + i * d for i in range(n)]
    y = [randint(-y0, y0) for i in range(n)]
                 
def show():
    for i in range(n):
        goto(x[i], y[i])
        dot(d)

create(20)
show()
```

**Exercice** Modifiez le nombre d'éléments.

## Visualiser un algorithme

Pour visualiser l'algorithme du minimum nous dessinons en rouge les valeurs du minimum courant.
Cet algorithme :

- prend la première valeur comme minimum courant,
- parcourt le reste de la liste,
- garde la valeur comme nouveau minimum si elle est plus petite.

```{codeplay}
from turtle import *
from random import *

color('blue')
speed(0)
up()

def create(size, bg='skyblue'):
    global n, d, x, y
    getscreen().bgcolor(bg)
    n = size
    d = 600/n
    x0 = 300 - d//2
    y0 = 200 - d//2
    x = [-x0 + i * d for i in range(n)]
    y = [randint(-y0, y0) for i in range(n)]
                 
def show():
    for i in range(n):
        goto(x[i], y[i])
        dot(d)
=== 
create(30)
show()

speed(3)
color('red')
for i in range(n):
    if i == 0:
        min = y[i]
    else:
        if y[i] < min:
            min = y[i]
    goto(x[i], min)
    down()
    dot(d/2)
```

**Exercice** : Modifiez l'algorithme pour trouver le maximum.

## L'indice du minimum

Souvent on ne doit pas seulement trouver la valeur minimum, mais aussi son indice dans la liste.
Différent au cas précédent, nous itérons pas sur les valeurs, mais sur les indices.

```{codeplay}
liste = [3, 4, 1, 2, 6, 5]

min = liste[0]
i_min = 0
n = len(liste)

for i in range(1, n):
    if liste[i] < min:
        min = liste[i]
        i_min = i
        
print(i_min)
```

**Exercice** : Modifiez l'algorithme pour trouver l'indice du maximum.

## Echanger deux éléments

Pour échanger deux éléments d'une liste nous utilisons une affectation multiple.
Ici nous échangeons les deux premiers éléments, donc les éléments avec les indices 0 et 1.

```{codeplay}
liste = [3, 4, 1, 2, 6, 5]

print(liste)
liste[0], liste[1] = liste[1], liste[0]
print(liste)
````

Le programme devient plus lisible si nous définissons une fonction `echange()`.

```{codeplay}
liste = [3, 4, 1, 2, 6, 5]

def echange(liste, i, j):
    liste[i], liste[j] = liste[j], liste[i]

print(liste)
echange(liste, 0, 2)
print(liste)
```

## Déplacer un point

Pour visualiser le déplacement d'un point de l'indice `i` vers l'indice `j` nous effaçons le premier point en le dessinant en blanc, et nous indiquons avec une ligne le déplacement vers la nouvelle position.

```{codeplay}
from turtle import *
from random import *

color('blue')
speed(0)
up()

def create(size, bg='skyblue'):
    global n, d, x, y
    getscreen().bgcolor(bg)
    n = size
    d = 600/n
    x0 = 300 - d//2
    y0 = 200 - d//2
    x = [-x0 + i * d for i in range(n)]
    y = [randint(-y0, y0) for i in range(n)]
                 
def show():
    for i in range(n):
        goto(x[i], y[i])
        dot(d)
===
def move(i, j):
    goto(x[i], y[i])
    color('white')
    dot(d)
    down()
    goto(x[j], y[i])
    color('blue')
    dot(d)
    up()

create(15)
show()

speed(3)
move(3, 13)
```

## Echanger deux points

Pour échanger deux points, il faut :

- déplacer point `i` vers `j`
- déplacer point `j` vers `i`
- échanger les deux éléments dans la liste

```{codeplay}
from turtle import *
from random import *

color('blue')
speed(0)
up()

def create(size, bg='skyblue'):
    global n, d, x, y
    getscreen().bgcolor(bg)
    n = size
    d = 600/n
    x0 = 300 - d//2
    y0 = 200 - d//2
    x = [-x0 + i * d for i in range(n)]
    y = [randint(-y0, y0) for i in range(n)]
                 
def show():
    for i in range(n):
        goto(x[i], y[i])
        dot(d)

def move(i, j):
    goto(x[i], y[i])
    color('white')
    dot(d)
    down()
    goto(x[j], y[i])
    color('blue')
    dot(d)
    up()
===
def swap(i, j):
    move(i, j)
    move(j, i)
    y[i], y[j] = y[j], y[i]

create(15)
show()

speed(3)
swap(3, 13)
```

## Echanger tous les points

Dans l'exemple suivant nous échangeons deux points successives pour toute la liste. Nous observons que :

- le premier point avance complètement de gauche à droite
- tous les autres points reculent d'une position

```{codeplay}
from turtle import *
from random import *

color('blue')
speed(0)
up()

def create(size, bg='skyblue'):
    global n, d, x, y
    getscreen().bgcolor(bg)
    n = size
    d = 600/n
    x0 = 300 - d//2
    y0 = 200 - d//2
    x = [-x0 + i * d for i in range(n)]
    y = [randint(-y0, y0) for i in range(n)]
                 
def show():
    for i in range(n):
        goto(x[i], y[i])
        dot(d)

def move(i, j):
    goto(x[i], y[i])
    color('white')
    dot(d)
    down()
    goto(x[j], y[i])
    color('blue')
    dot(d)
    up()

def swap(i, j):
    move(i, j)
    move(j, i)
    y[i], y[j] = y[j], y[i]
===
create(15)
show()

speed(3)
for i in range(n-1):
    swap(i, i+1)
```

## Tri par sélection

L’algorithme du tri par sélection commence par rechercher le plus petit élément de la liste et l’échange avec le premier élément de la liste.

```{codeplay}
liste = [3, 4, 1, 2, 6, 5]
print(liste)

def echange(liste, i, j):
    liste[i], liste[j] = liste[j], liste[i]

n = len(liste)
for i in range(n-1):
    i_min = i
    min = liste[i]
    for j in range(i+1, n):
        if liste[j] < liste[i_min]:
            i_min = j
            min = liste[j]
    echange(liste, i, i_min)
    print(liste)
```

Avec les fonctions `min()` et `index()` nous pouvons écrire cet algorithme de façon encore plus compact.

```{codeplay}
liste = [3, 4, 1, 2, 6, 5]

def tri_selection(liste):
    for i in range(0,len(liste)-1):
        i_min = liste.index(min(liste[i:]))
        liste[i], liste[i_min] = liste[i_min], liste[i]

print(liste)
tri_selection(liste)
print(liste)
```

Voici une visualisation du tri par séléction.

```{codeplay}
from turtle import *
from random import *

color('blue')
speed(0)
up()

def create(size, bg='skyblue'):
    global n, d, x, y
    getscreen().bgcolor(bg)
    n = size
    d = 600/n
    x0 = 300 - d//2
    y0 = 200 - d//2
    x = [-x0 + i * d for i in range(n)]
    y = [randint(-y0, y0) for i in range(n)]

def show():           
    for i in range(n):
        goto(x[i], y[i])
        dot(d)

def move(i, j):
    goto(x[i], y[i])
    color('white')
    dot(d)
    down()
    goto(x[j], y[i])
    color('blue')
    dot(d)
    up()

def swap(i, j):
    move(i, j)
    move(j, i)
    y[i], y[j] = y[j], y[i]
===
create(20)
show()

for i in range(n-1):
    i_min = i
    min = y[i]
    for j in range(i+1, n):
        if y[j] < y[i_min]:
            i_min = j
            min = y[j]
    swap(i, i_min)
show()
```

**Exercice** : Modifiez la taille de la liste.

## Tri par insertion

Le **tri par insertion** est un algorithme de tri utilisé par la plupart des personnes pour trier des cartes à jouer.

Ci-dessous mous trions une liste en ordre décroissante, ce qui permet de bien voir ce qui se passe.
On peut alors observer comment le `4` descend vers le bas, ensuite c'est le tour du `3` de descendre vers le bas, et ainsi de suite.

```{codeplay}
y = [5, 4, 3, 2, 1]
print(y)

n = len(y)
for i in range(1, n):
    for j in range(i, 0, -1):
        if y[j] < y[j-1]:
            y[j], y[j-1] = y[j-1], y[j]
        else:
            break
        print(y)
```

Voici une visualisation du tri par insértion.

```{codeplay}
from turtle import *
from random import *

color('blue')
speed(0)
up()

def create(size, bg='skyblue'):
    global n, d, x, y
    getscreen().bgcolor(bg)
    n = size
    d = 600/n
    x0 = 300 - d//2
    y0 = 200 - d//2
    x = [-x0 + i * d for i in range(n)]
    y = [randint(-y0, y0) for i in range(n)]

def show():          
    for i in range(n):
        goto(x[i], y[i])
        dot(d)

def move(i, j):
    goto(x[i], y[i])
    color('white')
    dot(d)
    down()
    goto(x[j], y[i])
    color('blue')
    dot(d)
    up()

def swap(i, j):
    move(i, j)
    move(j, i)
    y[i], y[j] = y[j], y[i]
===
create(20)
show()

for i in range(1, n):
    for j in range(i, 0, -1):
        while y[j] < y[j-1]:
            swap(j, j-1)
show()
```

**Exercice** : Modifiez la taille de la liste.

## Tri à bulles

L’algorithme du tri à bulles compare les éléments voisins, deux par deux, et les met dans le bon ordre.
Ci-dessous mous trions une liste en ordre décroissante, ce qui permet de bien voir ce qui se passe.

On peut alors observer comment le `5` flotte vers le haut, ensuite c'est le tour du `4` monte vers la surface, comme des bulles dans l'eau.

```{codeplay}
y = [5, 4, 3, 2, 1]
print(y)

n = len(y)
for i in range(n-1):
    for j in range(n-i-1):
        if y[j] > y[j+1]:
            y[j], y[j+1] = y[j+1], y[j]
        print(y)
```

Voici une visualisation du tri à bulles.

```{codeplay}
from turtle import *
from random import *

color('blue')
speed(0)
up()

def create(size, bg='skyblue'):
    global n, d, x, y
    getscreen().bgcolor(bg)
    n = size
    d = 600/n
    x0 = 300 - d//2
    y0 = 200 - d//2
    x = [-x0 + i * 600/n for i in range(n)]
    y = [randint(-y0, y0) for i in range(n)]

def show():              
    for i in range(n):
        goto(x[i], y[i])
        dot(d)

def move(i, j):
    goto(x[i], y[i])
    color('white')
    dot(d)
    down()
    goto(x[j], y[i])
    color('blue')
    dot(d)
    up()

def swap(i, j):
    move(i, j)
    move(j, i)
    y[i], y[j] = y[j], y[i]
===
create(20)
show()

for i in range(n-1):
    for j in range(n-i-1):
        if y[j] > y[j+1]:
            swap(j, j+1)
show()
```

**Exercice** : Modifiez la taille de la liste.

```{codeplay}

```

```{codeplay}

```

```{codeplay}

```

```{codeplay}

```

```{codeplay}

```

```{codeplay}

```

```{codeplay}

```

```{codeplay}

```

```{codeplay}

```