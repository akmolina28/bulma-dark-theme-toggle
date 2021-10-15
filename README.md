# bulma-dark-theme-toggle

Quick demonstration of a button to toggle light and dark Bulma themes. View the demo here: https://akmolina28.github.io/bulma-dark-theme-toggle/

Credit to https://github.com/jenil/bulmaswatch for the dark theme used in this demo.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

## How it works

Theme toggling works by using Sass to move the Bulma styles for each theme into different classes on the HTML tag. (see [app.scss](src/sass/app.scss))

When the Sass is compiled, instead of generating CSS rules like

```
.button.is-primary {
    background-color: #00d1b2;
    border-color: transparent;
    color: #fff;
}
```

This project generates

```
html.light-theme .button.is-primary {
    background-color: #00d1b2;
    border-color: transparent;
    color: #fff;
}

html.dark-theme .button.is-primary {
    background-color: #375a7f;
    border-color: transparent;
    color: #fff;
}
```
Finally, javascript can be used to toggle the class name on the html tag and the different styles will render instantly!

<br>

<a href="https://www.buymeacoffee.com/akmolina28" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 40px !important;width: 138px !important;" ></a>
