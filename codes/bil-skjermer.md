[<-- Tilbake](../README.md)

## Flere Skjermer

Lag flere skjermer.

Bruk en Hvis - blokk og CurrentScreen = (skjermnummer).
Skjermnuummeret starter på null, så skjermnummeret til skjerm nummer 2, blir 1.

```javascript
// Button Clicked
input.onButtonPressed(Button.A, function () {
    if (!(CurrentScreen == 0)) {
        CurrentScreen += -1
        ShowScreen()
    }
})
// Functions
function ShowScreen () {
    Screens[CurrentScreen].showImage(0)
}
input.onButtonPressed(Button.AB, function () {
    CurrentScreen = 0
    ShowScreen()
})
input.onButtonPressed(Button.B, function () {
    if (!(CurrentScreen == Screens.length - 1)) {
        CurrentScreen += 1
        ShowScreen()
    }
})
let CurrentScreen = 0
let Screens: Image[] = []
Screens = [images.iconImage(IconNames.Happy), images.iconImage(IconNames.Square), images.createImage(`
    . . # . .
    . # # # .
    # . # . #
    . . # . .
    . . # . .
    `), images.arrowImage(ArrowNames.SouthEast), images.iconImage(IconNames.Scissors)]
basic.clearScreen()
CurrentScreen = 0
ShowScreen()
```
