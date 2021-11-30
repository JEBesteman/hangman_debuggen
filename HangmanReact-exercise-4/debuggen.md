# Bug exercise 4: When the input field is empty it's still possible to guess that "letter"

## hoe bug te lokaliseren?

1. Als je geen letter invoert en op guess button klikt, neemt je aantal guesses af en wordt een lege string in WronglyGuessedLetters toegevoegd. Dat wil je niet!
2. Als je in TextInput kijkt zie je dat het input met props.submit door gegeven wordt aan App.js
3. In App.js zie je dat met submit={props.guessLetterHandler} dit weer doorgegevn wordt aan AppContainer
4. in guessLetterHandler wordt elke waarde gelijk aan state toegevoegd. Je wil een beperking hebben, zodat er een letter ingevoerd moet worden.
5. test code toevoegen die checkt of Textinput niet leeg is --> this.currentChosenLetter.length > 0;
6. Je kan dan geen lege input invoeren maar ook geen letter guessen.
7. test code toevoegen die checkt of guessedLetter niet includes is in currentChosenLetter...
8. werkt nu!!
