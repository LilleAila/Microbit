#Microbit Codes

##Input:
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

## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/LilleAila/Microbit/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

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

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/LilleAila/Microbit/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
