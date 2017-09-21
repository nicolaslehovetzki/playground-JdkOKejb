# Les enums
Voici une petite série d'exercices de Swift.
Vous pouvez écrire votre code dans le bloc prévu à cet effet et tester le résultat en cliquant sur *Run*.
Pour voir le corrigé, il suffit de déplier le bloc correspondant.

Exercices sur les `Enum`.

## `enum` et `struct`
* Créer un `struct` `Eleve`

Avec les propriétés : nom, age, sexe, niveau

Valeurs possibles pour le niveau : cp, ce1, ce2, cm1, cm2
Valeurs possibles pour le sexe : garcon, fille

* Mettre ces élèves dans un tableau

ecrire une fonction qui prend en entree un tableau d'eleve et un niveau : et qui renvoie un tableau composé des élèves de ce niveau
l'appliquer au tableau eleves pour tester

* Créez quelques élèves, par exemple :
toto, 6 ans, garcon, cp
kiki, 8 ans, fille, ce2
lolo, 9 ans, garcon cp


```swift runnable
// Vous pouvez taper votre code ici
```
::: Indices
* Utilisez des `enum` pour le sexe et le niveau
* Attention aux types de variables à manipuler
:::

::: Corrigé
```swift runnable
enum Sexe {
    case garcon, fille
}

enum Niveau {
    case cp, ce1, ce2, cm1, cm2
}

struct Eleve {
    var nom: String
    var age: Int
    var sexe: Sexe
    var niveau: Niveau
}

let toto = Eleve(nom: "Toto", age: 6, sexe: .garcon, niveau: .cp)
let kiki = Eleve(nom: "kiki", age: 8, sexe: .fille, niveau: .ce1)
let lolo = Eleve(nom: "Lolo", age: 9, sexe: .garcon, niveau: .ce2)

let eleves = [toto, kiki, lolo]

func select(eleves: [Eleve], niveau: Niveau) -> [String] {
    var output = [String]()
    for eleve in eleves {
        if eleve.niveau == niveau {
            output.append(eleve.nom)
        }
    }
    return output
}

print(select(eleves: eleves, niveau: .cp))
```