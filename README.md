# vuetifyjs-dynamic-theme-example

> This is test of dynamic CSS variables usage in Vuetify. See [demo online](https://darosh.github.io/vuetifyjs-dynamic-theme-example/dist/).


## Browser issues

Theme switch is disabled by feature and browser detection where needed.

### IE

Black & White as [expected](http://caniuse.com/css-variables/embed).

### Edge

Broken Badges and Picker. My guess it has something to do with ```::before```, ```::after``` CSS selectors. 

It loads style without CSS variables and the theme switch is disabled. 

## Contrast issues

Unfortunately there is no text automatic color, which may lead to bad [usability](https://material.io/guidelines/style/color.html#color-color-system).

## How it works?

### [./src/stylus/main.styl](src/stylus/main.stylus) file:

```styl
@import '../../node_modules/vuetify/src/stylus/settings/_colors'

body {
  --primary: $blue.darken-2;
  --accent: $amber.accent-3;
  --secondary: $grey.base;

  --info: $blue.base;
  --warning: $amber.base;
  --error: $red.accent-2;
  --success: $green.base;
}

$theme := {
  primary: var(--primary)
  accent: var(--accent)
  secondary: var(--secondary)

  info: var(--info)
  warning: var(--warning)
  error: var(--error)
  success: var(--success)
}

@import '../../node_modules/vuetify/src/stylus/main'
```

### [./src/App.vue](./src/App.vue) file:

```js
setTheme (theme) {
  document.body.style.setProperty('--primary', theme[0])
  document.body.style.setProperty('--accent', theme[1])
  document.body.style.setProperty('--secondary', theme[2])
}
```

### Fix in ```./node_modules/vuetify/src/stylus/tools/_progress-linear.styl``` source needed:

```styl
progress-linear(progress)
  .progress-linear__bar
    //background: lighten(progress, 50%)
    background: lighten(black, 87.5%)
```

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
