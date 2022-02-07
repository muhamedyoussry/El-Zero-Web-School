<h1 align="center">CSS El Zero Web School</h1>


## My Notes
- start your style element with `selector` and inside selector you wrote some `properties`, inside every `property` you have many `values`.
- add `;` at the end of the line.
- we use `#` for id selector and we use `.` for class selector.
- styling types
  - ixternal style - inside an external CSS file
  - internal style - inside the HTML file
  - inline style - inside the HTML elemen
- use `background-size` to make the image take the full element or the full screen.
- `padding` property for the 4 directions: top right bottom left
- `margin` accepts negative values but `padding` do not accept negative values.
- `margin: auto;` used to align the element content to the center.
- `border-radius` can be used for profile picture photos.
- 


<h2 align="center">Assignment 1</h2>

### Question 1
``` CSS
/* Any Element With Class Title */
.title {
}

/* Any element with the id nav */
#nav {
}

/* Any div element */
div {
}

/* Any h2 element */
h2 {
}
```

## Question 2

```HTML
<!-- external CSS style inside CSS file -->
<link rel="stylesheet" href="css/file.css" />

<!-- internal CSS style inside the HTML -->
<style>
p {
  color: red;
}
</style>

<!-- Inline CSS style -->
<p style="color: blue;">This Is Our Paragraph</p>
```

## Question 3

```HTML
<link rel="styleshete" href="./assets/master.css" />
```

## Question 4

```HTML
<link rel="styleshete" href="../source/css/main.css" />
```
## Question 5

```CSS
/* valid */
._user-name {
}

/* valid */
.-user-name {
}

/* not valid */
.1user-name {
}

/* not valid */
.@user-name {
}

/* not valid */
.user@name {
}

/* valid */
._user10name {
}

/* valid */
.u {
}
```

## Question 6

```CSS
/* Bad */
.USERNAME {
}

/* Bad */
.UserName {
}

/* GOod */
.user-name {
}

/* Bad */
.userName {
}

/* Bad */
.usernameprofile {
}
```

<h2 align="center">Assignment 2</h2>

## Question 1

```css
div.assign-1-shape-1 {
    background-color: hsl(271, 76%, 53%);
    background-color: rgba(138, 44, 226, 1);
    background-color: #8a2ce2;
    width: 500px;
    margin: 10px auto;
    padding: 20px;
}

div.assign-1-shape-2 {
    background-color: rgba(138, 44, 226, 0.5);
    width: 500px;
    margin: 10px auto;
    padding: 20px;
}

div.assign-1-shape-3 {
    background-color: rgba(138, 44, 226, 0.1);
    width: 500px;
    margin: 10px auto;
    padding: 20px;
}
```
## Question 2

```css
div {
    width: 400px;
    height: 400px;
    background-image: url(./css-assignment-5-8.png);
}

div.assign-1-shape-1 {
    background-repeat: no-repeat;
}

div.assign-1-shape-2 {
    background-repeat: repeat-y;
}

div.assign-1-shape-3 {
    background-repeat: repeat-x;
}

div.assign-1-shape-4 {
    background-repeat: repeat;
}
```

## Question 3

```css
div {
    width: 400px;
    height: 400px;
    background-image: url(./css-assignment-5-8.png);
    color: gray;
    font-size: 20px;
    margin: 10px;
}

div.assign-1-shape-1 {
    background-repeat: no-repeat;
}

div.assign-1-shape-2 {
    background-repeat: repeat-y;
    background-position: right;
}

div.assign-1-shape-3 {
    background-repeat: repeat-x;
    background-position: bottom;
}

div.assign-1-shape-4 {
    background-repeat: repeat;
}
```

## Question 4

```css
div {
    width: 400px;
    height: 400px;
    background-image: url(./css-assignment-5-8.png);
    color: gray;
    font-size: 20px;
    margin: 10px;
}

div.assign-1-shape-1 {
    background-repeat: no-repeat;
    background-size: 80%;
}

div.assign-1-shape-2 {
    background-repeat: repeat-y;
    background-position: right;
    background-size: 75%;
}

div.assign-1-shape-3 {
    background-repeat: repeat-x;
    background-position: bottom;
    background-size: 75%;
}

div.assign-1-shape-4 {
    background-repeat: no-repeat;
    background-position: right bottom;
    background-size: 50% 50%;
}
```