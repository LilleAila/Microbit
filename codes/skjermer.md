[<-- Tilbake](../README.md)

##Skjermer

```javascript
// Pins Clicked
input.onPinPressed(TouchPin.P0, function () {
    if (CurrentScreen == 0) {
        Screens[0] = images.arrowImage(ArrowNames.NorthWest)
        ShowScreen();
    } else if (CurrentScreen == 1) {
        if(Speed != 0) {
            Speed -= 1;
            ShowSpeed();
        }
    }
})

input.onPinPressed(TouchPin.P1, function () {
    if (CurrentScreen == 0) {
        Screens[0] = images.arrowImage(ArrowNames.North)
        ShowScreen();
    } else if (CurrentScreen == 1) {
        Speed = 0;
        ShowSpeed();
    }
})

input.onPinPressed(TouchPin.P2, function () {
    if (CurrentScreen == 0) {
        Screens[0] = images.arrowImage(ArrowNames.NorthEast)
        ShowScreen()
    } else if (CurrentScreen == 1) {
        if(Speed != 15) {
            Speed += 1;
            ShowSpeed();
        }
    }
})

//Forever
basic.forever(function() {
    if(CurrentScreen == 1) {
        //ShowSpeed();
    } else {
        
    }
})

//Functions
function ShowSpeed() {
    basic.clearScreen();
    led.plot(2, 2);
    if(Speed != 0) {
        for(let i = 0; i < Speed; i++) {
            led.plot(SpeedLights[i][0], SpeedLights[i][1]);
        }
    }
}

function ShowScreen() {
    Screens[CurrentScreen].showImage(0);
}

// Button Clicked
input.onButtonPressed(Button.A, function () {
    if (!(CurrentScreen == 0)) {
        CurrentScreen += -1;
        ShowScreen();
    }
})

input.onButtonPressed(Button.B, function () {
    if (!(CurrentScreen == Screens.length - 1)) {
        CurrentScreen += 1;
        ShowScreen();
    }
})

input.onButtonPressed(Button.AB, function () {
    CurrentScreen = 0;
    ShowScreen();
})

//On Start
let CurrentScreen = 0
let Screens: Image[] = []
Screens = [images.arrowImage(ArrowNames.North), images.createImage(`
    . . . . .
    . . . . .
    . . # . .
    . . . . .
    . . . . .
    `)]
let Speed = 0;
let SpeedLights = [[0, 0], [1, 0], [2, 0], [3, 0], [4, 0], [4, 1], [4, 2], [4, 3], [4, 4], [3, 4], [2, 4], [1, 4], [0, 4], [0, 3], [0, 2]]
basic.clearScreen()
CurrentScreen = 0
ShowScreen()
```
