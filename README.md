# Microbit Codes

## Input:
```javascript
basic.clearScreen()
radio.setGroup(1)
led.unplot(2, 0)
led.unplot(2, 2)
led.unplot(2, 4)
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

```


### Markdown
```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```
