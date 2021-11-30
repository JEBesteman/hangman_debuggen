# Excercise 2: it's not possible to guess a letter

## Hoe ga ik de bug vinden?

1. Eerst uitproberen waneer fout optreedt.
2. Als je een letter wil invoeren, kan dit niet, refreshed de pagina gelijk.
3. Met Chrome devTools zie je in console gelijk een foutmelding: Uncaught TypeError: this.state.guesedLetters is not iterable.
4. TypeError: op zoek naar typefout in AppContainer.js en dan voornamelijk in guessLetterHandler.
5. VSCode geeft aan met ... onder [...this.state.guesedLetters] aan dat er iets niet klopt.
6. Moet guessedLetters zijn ipv guesedLetters.
7. Typefout veranderd, werkt nu!
