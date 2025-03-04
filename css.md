## CSS

### 1. Inline CSS
`style` attribute is used to define CSS properties at each HTML element.
```html
<h1 style = "color:blue; font-size:40px; font-style: italic;"> One Compiler </h1>
```

### 2. Internal CSS
You can define CSS properties using `<style>` tag in `<head>` section.

```html
<head>
<style>
body {background-color: pink;}
h1   {color: red;}
h2    {color: green; font-size : 40px; font-style: italic;}
</style>
</head>
```

### 3. External CSS

`<link>` tag is used to refer an external CSS file.

```html
 <link rel="stylesheet" href="styles.css" />
```

### 4. CSS Selectors
you can select elements based on their name 

```css
    div {
        font-familt:'Inter',sans-serrif;
        max-width:400px;
    }
```
or you can use both class based or id base css selection 
```css
    // classed based 
    .container {
        background:red;
        height:600px;
    }
    // id based
    #container {
        background:purple;
        margin:10px;
    }

```


### 5. FlexBox
you can use Flexbox to properly align your elements 

to use Flexbox give this property to the parent element

```css
    .parent {
        display:flex;
    }
```

to align the elements towards the main axis By default it's horizontail we use 

<b>Justify-content</b>

| Vlaues |  | description |
|----|----|---|
| flex-start |  | Items are packed towards the start  | 
| center |  | Items are packed on the center  | 
| flex-end |  | Items are packed towards the end  | 
| space-around | | Items are equally distributed with equal space aroun them |
| space-between| | items are evenly distributed .first item at the start and last items at the end |
| space-evenly | | Items are evenly spaced with same amount space between them | 

to align the elments towards the cross-axis we use

<b>Align-items</b>


| Vlaues |  | description |
|----|----|---|
| flex-start |  | Items are packed towards the start of cross axis  | 
| center |  | Items are packed on the center of cross axis  | 
| flex-end |  | Items are packed towards the end of the cross axis  | 

By default flex works in a horizontal way to use flex in a vartical way use

### <b>The direction of flex is consider the main axis and the other axis consider as cross axis</b>

```css 
    .parent {
        display:flex;
        flex-direction:column;
    }
```

### 6. CSS Grid
Css grid is another way to properly align your html elements

to create a new  grid use  
```css
    .box {
        display:grid;
    }
```
grid are made of two things columns and rows  using <b>grid-template-rows</b> and <b>grid-template-columns</b> you can define how many rows and columns you want 
```css 
    .box {
        display:grid;
        grid-template-columns:400px 300px 200px;
        grid-template-rows:50px 70px  60px;
    }

```

you can use grid using a special unit called  <b>Fr (fraction)</b> which means portions of remaining space
```css 
    .box {
        display:grid;
        grid-template-columns:1fr 1fr 1fr;
        // or 
        grid-template-columns: repeat(3,1fr)
    }
```