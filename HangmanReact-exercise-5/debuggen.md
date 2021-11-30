# Bug exercise 5: You can continue guessing until -1 guesses

## Waar zit de bug??

1. Je kan letters in blijven voeren totdat je aantal guesses -1 is. Dus een keer teveel raden.
2. GuessesLeft = props.maxGuesses - props.wrongLetters.length.
3. maxGuesses staat op 5, ook in state dus dat is het niet
4. wrongLetters.length --> WronglyGuessedLetters state is gewoon goed, verkeerde gekozen letters worden toegevoegd. klopt dus.
5. In App.js kijken: const isGameOver --> gameOver true als woord geraden is of als getWrongLetters(game.chosenWord, game.guessedLetters).length > game.maxGuesses. Laatste klopt niet, moet >= zijn. Spelletje moet al over zijn, als length gelijk is aan maxGuesses.
