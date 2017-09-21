# Petits exercices de Swift

### Exercice 1 
Ecrire une fonction qui prend en entrée un tableau d'entiers et renvoie un tableau constitué des nombres positifs de ce tableau

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


### Quizz

?[Vous avez aimé ?]
-[x] Yes, trop cool
-[ ] Non

`let c = 4`
