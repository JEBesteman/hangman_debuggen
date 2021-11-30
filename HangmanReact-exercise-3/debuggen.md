# Bug exercise 3: When the game starts it's won immediately

## Uitvinden waar de bug zit

1. Als je het spelletje laat, zie je gelijk dat je gewonnen hebt.
2. In react devTools zie je in dat bij GameOver component, wordGuessed: true staat. Dit klopt niet!
3. In App.js code wordGuessed bekijken.
4. 2 console.logs erin gezet: remaining en remaining.length --> remaining = [] en remaining.length = 0. Vreemd
5. return remaining.length === 0; even uitgecommented. zodat spel gewoon van start gaat
6. Als je nu een letter invoert, wordt de letter toegevoegd tot remaining en remaining.length wordt 1. Klopt niet!!
7. Ik denk dat het aan de filter methode ligt. Je wilt de goed gekozen letter niet in de nieuwe array (remaining) hebben (false returnen) en hij returnt nu true, want wordt toegevoegd aan remaining.
8. Als je nu in filter method: !guessedLetters.includes(letter) maakt ipv guessedLetters.includes(letter) dan wordt de goed gekozen letter niet gereturnd in remaining.
9. return remaining.length === 0; weer erbij zetten en dan werkt het weer!!
