# Petits exercices de Swift

### Exercice 1 
Ecrire une fonction qui prend en entrée un tableau d'entiers et renvoie un tableau constitué des nombres positifs de ce tableau.

```swift runnable
// Vous pouvez taper votre code ici

```

::: Corrigé
```swift runnable
func filterPositives(numbers:[Int]) -> [Int] {
    var output = [Int]()
    
    for number in numbers {
        if number >= 0 {
            output.append(number)
        }
    }
    return output
}
print(filterPositives(numbers: [4, 8, 0, -4, 7]))

```
:::

### Exercice 2
Ecrire une fonction qui prend en entrée le nom de l'utilisateur, son age et renvoie une string : "bienvenue ..." si la personne est majeure et nil si la personne est mineure.

```swift runnable
// Vous pouvez taper votre code ici

```

::: Corrigé
```swift runnable
func getWelcomeMessage(name: String, age: Int) -> String? {
    if age >= 18 {
        return "Bienvenue \(name)"
    } else {
        return nil
    }
}
let message = getWelcomeMessage(name: "Toto", age: 25)
if message != nil {
    print(message as Any)
}
```
:::

### Exercice 3
En utilisant une boucle, remplir un tableau comme ceci [10, 9, 8, 7, 6, 5, 4, 3, 2, 1].

```swift runnable
// Vous pouvez taper votre code ici

```

::: Corrigé
```swift runnable
var numbers = [Int]()
for index in 1...10 {
    numbers.append(11 - index)
}
print(numbers)
```
:::


### Quizz

?[Vous avez aimé ?]
-[x] Yes, trop cool
-[ ] Non

