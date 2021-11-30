# Bug exercise 1

Problem: When the word is guessed correctly, you still lose

## Hoe bug te vinden?

1. Eerst uitvinden wanneer de fout gebeurd.
2. Als je het goede woord invult met gebruik van console.log, daar staat het gekozen woord. Dan verlies je toch!
3. Ik bekijk met react devTools de state.
4. Alles lijkt goed te gaan qua gekozen letters. Maar als je bij GameOver kijkt, zie je dat wordGuesed: true staat. Dat klopt maar dan is het dus raar dat je een lose gifje krijgt.
5. Dus ga ik GameOver.js bekijken.
6. Variabelen lijken oke te zijn. Dus console.log("woord geraden", props.wordGuessed) op regel 20 om te kijken wat er mee gegeven wordt via de props.
7. Je verwacht true, maar je krijgt undefined!!
8. Dus de state wordt niet goed doorgegeven via props.
9. Als je in react devTools en App.js kijkt zie je datprops.wordGuesed wordt meegegeven. Als je dat console.log in GameOver krijgt je wel true.
10. In App.js wordGuesed verandert in wordGuessed.
11. Nu werkt het wel!! Ook als je een fout antwoord geeft.
