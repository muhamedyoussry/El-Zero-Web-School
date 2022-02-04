<h1 align="center">CSS El Zero Web School</h1>


## My Notes
- start your style element with `selector` and inside selector you wrote some `properties`, inside every `property` you have many `values`.
- add `;` at the end of the line.
- we use `#` for id selector and we use `.` for class selector.
- styling types
  - ixternal style - inside an external CSS file
  - internal style - inside the HTML file
  - inline style - inside the HTML elemen
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