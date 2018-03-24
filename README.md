# Importing fonts

### Through CDN

##### (1) `index.html`

```html
<head>
  <title>Your page</title>
  <!-- Font Awesome https://fontawesome.com/icons?d=gallery&m=free -->
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">


  <!-- Google Fonts https://fonts.google.com/?selection.family=Roboto -->
  <link href="https://fonts.googleapis.com/css?family=Roboto" rel="stylesheet">


  <!-- Your stylesheet AFTER importing the fonts -->

  <link rel="stylesheet" href="./css/styles.css">
</head>

```

##### in `styles.css`

```css
body {
  font-family: 'Roboto'
}
```

### Local

##### Include font files
(example)
```
- index.html
|
|---/fonts
|   |
|   |---/Fantasque
|       |---Fantasque.eot
|       |---Fantasque.woff
|       |---Fantasque.woff2
|       |---Fantasque-Bold.eot
|       |---Fantasque-Bold.woff
|       |---Fantasque-Bold.woff2
|       ....
|
|---css
|     |---styles.css
```

##### In `styles.css`
- import with `@font-face`

```css

@font-face {
  font-family: 'Fantasque Sans Mono';
  src: url('../fonts/fantasque/FantasqueSansMono-Regular.eot'); /* IE 9 Compatibility Mode */
  src: url('../fonts/fantasque/FantasqueSansMono-Regular.eot?#iefix') format('embedded-opentype'), /* IE < 9 */
  url('../fonts/fantasque/FantasqueSansMono-Regular.woff2') format('woff2'),
  url('../fonts/fantasque/FantasqueSansMono-Regular.woff') format('woff'), /* Firefox >= 3.6, any other modern browser */
  url('../fonts/fantasque/FantasqueSansMono-Regular.ttf') format('truetype'), /* Safari, Android, iOS */
  url('../fonts/fantasque/FantasqueSansMono-Regular.svg#FantasqueSansMono-Regular') format('svg'); /* Chrome < 4, Legacy iOS */
  font-weight: 400;
  font-style: normal;
}


body {
  font-family: 'Fantasque Sans Mono'
}

p {
  font-size: 45px;
  font-style: italic;
  font-family: 700;
}

```
