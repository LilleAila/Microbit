[<-- Tilbake](../README.md)

## Input

Forskjellige måter å trykke knapper.

```javascript
input.onPinPressed(TouchPin.P0, function () {
    lastLastPress = lastPress
    lastPress = currentPress
    currentPress = "P0"
    if (currentPress == "P0" && (lastPress == "P1" && lastLastPress == "P2")) {
        canResetSwipe = true
        resetSwipe()
        led.plot(0, 4)
        basic.pause(1000)
        led.unplot(0, 4)
    } else {
        canResetSwipe = true
        basic.pause(700)
        resetSwipe()
    }
})
function resetSwipe () {
    if (canResetSwipe) {
        currentPress = "P0"
        lastPress = "P0"
        lastLastPress = "P0"
        canResetSwipe = false
    }
}
input.onPinPressed(TouchPin.P2, function () {
    lastLastPress = lastPress
    lastPress = currentPress
    currentPress = "P2"
    if (currentPress == "P2" && (lastPress == "P1" && lastLastPress == "P0")) {
        canResetSwipe = true
        resetSwipe()
        led.plot(4, 4)
        basic.pause(1000)
        led.unplot(4, 4)
    } else {
        canResetSwipe = true
        basic.pause(700)
        resetSwipe()
    }
})
input.onPinPressed(TouchPin.P1, function () {
    lastLastPress = lastPress
    lastPress = currentPress
    currentPress = "P1"
})
let currentPress = ""
let lastPress = ""
let lastLastPress = ""
let canResetSwipe = false
basic.clearScreen()
canResetSwipe = true
resetSwipe()
basic.forever(function () {
    if (input.pinIsPressed(TouchPin.P1)) {
        led.plot(2, 2)
    } else {
        led.unplot(2, 2)
    }
})
basic.forever(function () {
    if (input.buttonIsPressed(Button.A)) {
        led.plot(0, 2)
    } else {
        led.unplot(0, 2)
    }
})
basic.forever(function () {
    if (input.buttonIsPressed(Button.B)) {
        led.plot(4, 2)
    } else {
        led.unplot(4, 2)
    }
})
basic.forever(function () {
    if (input.pinIsPressed(TouchPin.P2)) {
        led.plot(2, 4)
    } else {
        led.unplot(2, 4)
    }
})
basic.forever(function () {
    if (input.isGesture(Gesture.Shake)) {
        led.plot(0, 0)
    } else {
        led.unplot(0, 0)
    }
})
basic.forever(function () {
    if (input.pinIsPressed(TouchPin.P0)) {
        led.plot(2, 0)
    } else {
        led.unplot(2, 0)
    }
})
basic.forever(function () {
    if (input.isGesture(Gesture.TiltLeft)) {
        led.plot(3, 0)
    } else {
        led.unplot(3, 0)
    }
})
basic.forever(function () {
    if (input.isGesture(Gesture.TiltRight)) {
        led.plot(4, 0)
    } else {
        led.unplot(4, 0)
    }
})

```
