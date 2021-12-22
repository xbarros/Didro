# Attendre - `while`

La boucle `while` est souvent utilisé pour attendre quelque chose.
Elle répète un bloc tant qu'une condition est vraie.

## Compteur à rebours

On peut utiliser la boucle `while` pour créer un compteur à rebours.
Pour attendre une seconde, la fonction `sleep()` du module `time` est importée.

```{codeplay}
from time import sleep

n = int(input('Entrez un entier: '))
while n > 0:
    print(n)
    sleep(1)
    n = n - 1

print('boum!!!')
```

## Lister des noms

Nous utilisons une boucle `while` pour demander des noms à l'utilisateur.
On ne peut pas savoir à l'avance combien de noms il y aura, donc ici nous ne pouvons pas utiliser la boucle `for`.  Nous prenons comme condition de terminaison une réponse avec une chaîne vide (`''`).

La convention est d'utiliser des noms au pluriel (`noms`) pour désigner la liste et le même nom au singulier (`nom`) pour désigner un de ses éléments.

```{codeplay}
noms = []
nom = input('Entrez un nom: ')

while nom != '':
    noms.append(nom)
    nom = input('Entrez un nom: ')
    
print(noms)
```

**Exercice** : Entrez les noms de 3-4 de vos amis.

## Faire une somme

Nous utilisons une boucle `while` pour demander des nombres à l'utilisateur. 
On ne peut pas savoir à l'avance combien de nombres il y aura, et donc nous ne pouvons pas utiliser la boucle `for`. Nous prenons comme condition de terminaison une réponse avec une chaîne vide (`''`).

Au lieu d'écrire `while x != '':` nous pouvons simplifier vers  `while x:`. 
La raison est que la chaîne vide est associée à `False` et toute autre chaîne non-vide est associée à `True`.

```{codeplay}
somme = 0
x = input('Entrez un nombre: ')

while x:
    somme += float(x)
    x = input('Entrez un nombre: ')
    
print('somme =', somme)
```

**Exercice** : Entrez les frais de vos 3 derniers achats.

## Faire une moyenne

Nous utilisons une boucle `while` pour demander des nombres à l'utilisateur. 
On ne peut pas savoir à l'avance combien de nombres il y aura, et donc nous ne pouvons pas utiliser la boucle `for`.  Nous prenons comme condition de terminaison une réponse avec une chaîne vide (`''`).

```{codeplay}
somme = 0
n = 0
x = input('Entrez un nombre: ')

while x:
    somme += float(x)
    n += 1
    x = input('Entrez un nombre: ')
    
print('moyenne =', somme/n)
```

**Exercice** : Entrez vos notes de français.

## Deviner un nombre

On peut aussi l'utiliser pour deviner un nombre.
Ici on importe la fonction `randint()` du module `random`.
Elle fournit un nombre entier aléatoire entre deux bornes (1, 99).

La fonction `input()` ne retourne que le type `string`.
La fonction `int()` transforme le type string (chaine) en entier (integer).

```{codeplay}
from random import randint

n = randint(1, 99)
x = int(input('Devinez un nombre entre 1 et 99: '))

while x !=  n:
    if x > n:
        print(x, 'est trop grand')
    else:
        print(x, 'est trop petit')
        
    x = int(input('Entrez un nombre: '))

print('\nBravo. Vous avez réussi!')
```

**Exercice** : Quel est la meilleure stratégie pour deviner un nombre ?


## Indentation

On appelle **bloc** une ou plusieurs instructions qui forment un ensemble.
En C ou JavaScript un bloc est délimité avec des accolades `{...}`.
L'indentation est encouragé mais reste optionnelle.

En Python l'indentation est obligatoire. C'est la façon officielle de designer un bloc.
Ceci présente deux avantages :

- pas besoin d'accolades pour délimiter une bloc,
- la structure des blocs est claire et visuelle.

Une **indentation** est un retrait du code par rapport à la marge gauche de 4 caractères.
Elle peut être insérée avec la touche tabulateur **TAB** (symbolisée par une flèche à gauche du clavier).

Une suite d'instructions indentées de la même manière forme un bloc.
Ces blocs se trouvent dans :

- la définition de fonction (`def`),
- l'instruction conditionnelle (`if-else`),
- la boucles (`for`, `while`).

En Python le symbole `:` en fin de ligne introduit un sous-bloc qui doit être indenté.
Voici 5 sous-blocs à la suite des 5 mot-clés `def`, `if`, `elif`, `else`, `for` :

```{codeplay}
def f(x):
    if x > 0:
        return 'positif'
    elif x < 0:
        return 'négatif'
    else:
        return 'zéro'

for i in range(-2, 2):
    print(i, f(i)) 
```

Dans l'exemple suivant nous avons une boucle qui fait trois itérations.
Les deux instructions `print()` font partie du bloc de la boucle.

```{codeplay}
for i in range(3):
    print('itération', i)
    print('-' * 11)
```

**Exercice** : Enlevez l'indentation de l'instructions `print('-' * 11)`.