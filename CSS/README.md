# CSS

Css is all about `properties: value` pair

properties like: `color`, `font-size`, `font-weight`..., 
and the properties value like `color: #000`, `font-size: 19px`, `font-weight: 300` 

css fundamentals

- Types of CSS
- Box Model
- Responsive
- flexbox
- CSS grid

css Syntax:

```css
body{
    /* properties: value; this is the way of commenting in css*/
    font-size: 62.5%;
}
```

css Types

- Inline css

```html
<p style="color: red">This paragraph color will be in red</p>

```

- Internal css

```html
<head>
    <style>
        p{
            color: red;
        }
    </style>
</head>
<body>
    <p>This paragraph color will be in red</p>
</body>

```

- External css

```css
/* style.css */

    p{
        color: red;
    }

```

## Properties and values

## Color in css

There are several different way to specify color in css:

- Color keyword
- RGB value
- RGBA value
- HSL value
- HSLA value
- Hexadecimal value

### Color Keyword

There are predefined color keyword in css like `red`, `blue`, `green`, `darkgray / darkgrey`, ...

```css
body{
    background-color: orange;
}
```

### RGA value

`RGB`, which stands for `red`, `green`, and `blue` is the color model that monitors use. Since in web design we're primarily concerned with what web pages look like on screens,

- RGB colors have three values that represent: `red`, `green`, and `blue`
- Each value can be a number between `0 and 255` or a percentage from `0 to 100%`
- A value of `0 means none of that color` is being used it will be `black`
- A `255 for all three color` values will be `white`

```css
    p {  color: rgb(0, 0, 0); }         /* black */
    h1 { color: rgb(255, 255, 255); }   /* white */
```

### RGBA color

`RGBA`, which stands for `red`, `green`, `blue` with `Alpha` channel

- The alpha value represents the `level of transparency` that the rgb color should have. It can be a value from `0 to 1` or a percentage from `0 to 100%`. Note that you must specify RGBA instead of RGB.

```css
    p{
        color: rgba(0, 0, 0, 0.2); 
    }
```

### HSL

`HSL` stands for `hue`, `saturation`, and `lightness` its awesome when working with shades and color adjustments.

```css
h1 {
   color: hsl(39, 100%, 50%) /*orange*/
}
```

### HSLA

`HSLA` is simply the HSL color model with the addition of an `alpha` channel.

```css
h1{
    color: hsla(39, 100%, 50%, 0.5);
}
```

### Hexadecimal Color

`Hex` values are actually just a different way to represent RGB values. Instead of using three numbers between 0 and 255, you use six hexadecimal numbers. Hex numbers can be `0-9` and `A-F`. Hex values are always prefixed with a `#` symbol.

```css
p  { color: #000000; }          /* black */
h1 { color: #ffffff; }          /* white */
h2 { color: #ff4500; }          /*orangered*/
```

## Descendant Selectors

<!-- Selects only the paragraphs contained within a section -->
```css
section p{ ... }
```

```HTML
<section>
  <p> ... </p>
</section>
<p> ... </p>
<p> ... </p>
```

## A selector in CSS

- A tag references an HTML tag
- A class references the `class` attribute on an HTML tag
- An ID references the `id` attribute on an HTML tag

```html
<!-- tag -->
<section>
    <!-- class -->
    <div class="wrapper">
        <!-- id -->
        <a href="url" id="link">Click me!</a>
    </div>
</section>
```

## Grouping Selectors

```css
/* applies to all h1 elements */
h1{ ... }

/* applies to any element with this class  */
.class { ... }

/* applies to both h1 and h2 elements  */
.h1, h2 { ... }

```

## Combining selector

```css
<!-- only applies if "fancy" and "intro" classes are included -->
.fancy.intro{ ... }
```

```HTML
<p class="fancy intro"> FANCY intro para</p>

<!-- applies to any elemnt with this class -->
.intro{
    color:blue;
}
<!-- only applies to <p> elemnt with this class -->
p.intro{
    font-size: 15px;
}

<p class="intro"> FANCY intro para</p>
```

## Inheritance

Css style can be Inherited from the ancestor to descendant elemnets

## Specificity

Specificity determines how browsers decide which CSS rules takes precendence.

1. universal selector (*)
2. type (p)
3. class (.example)
4. id (#example)

```CSS
* { color:red; }

p { color:green; }

.example{ color:black; }

#example{
    /* id selector override them all */
    color:blue; 
}

/* 
    Specificity Calculator
    A visual way to understand CSS specificity.  
    
    https://specificity.keegan.st/
*/

```

## Position in CSS

The position CSS property sets how an element is positioned in a document. The `top`, `right`, `bottom`, and `left` properties determine the location of elements.

A `relatively positioned` element is positioned relative to its normal position. The `top and bottom` properties specify the `vertical offset` from its normal position; the `left and right` properties specify the `horizontal offset`.

An `absolutely positioned` element is positioned relative to the first parent element that has a position other than static. The element is removed from the normal document flow, the box's offsets further can be specified using one or more of the properties `top`, `right`, `bottom`, and `left`.

![relative, absolute](/img/position-relative-absolute.png)

`Fixed positioning` is a subcategory of absolute positioning.
The only difference is, a fixed positioned element is `fixed` with respect to the browser's viewport and does not move when scrolled.

## css Unit

Absolute:

- fixed unit, always the same size
- Not affected by gthe values in related elements
- Example:
  - pixel px
  - Inches in
  - centimeter cm
  - milimeter mm
  - point pt
  - picas pc

Relative

- relational size, not fixed
- Dependent upon values declared in parent and ancestor elements
- Example:
  - percentage %
  - font size em & rem
  - character-size ex & ch

  - viewport Dimentions vw & vh
  - Viewport-max vmax
  - Viewport-min vmin

Unitless Value

- Some numeric values do not require a unit
- example:
  - line-heigh: 1.25;
  - font-weight: 300

<!-- 1st percentage-->

```css
        .parent{
            background-color: turquoise;
            height: 500px;
            width: 500px;
        }
        .child{
            background-color: rgba(0, 0, 0, 0.603);
            /* 1st */
            /* width: 50%; */
            height: 50%;
            /* 2nd */
            width: 100%;
            /* 2nd (a */
            padding: 5px;
            /* 2nd (b fix issue by using box-sizing  */
            box-sizing: border-box;
        }
```

<!-- 2nd View port -->
they divided the view port into 100x100 grid

```css
        .vw{
            background-color: wheat;
            height: 50vh;
            /* even if the browser shrink it will still be 50 of view port */
            width: 50vw;
        }
```

```css
        .vmin{
            background-color: aqua;
            height: 400px;
            width: 50vmin;
            /* it will response to height as well visa versa */
        }
```

<!-- 3rd font based unit-->

```css
        .ex{
            background-color: antiquewhite;
            width: 50%;
            height: 5ex;
            font-size: 20px;
        }
```

```css
        .example{
            font-size: 10px;
        }
        /* now 1 em is = to 1px because of parent fs 10px */
        .em{
            background-color: coral;
            width: 2em;
            height: 2em;
        }
```

```css
        .example{
            font-size: 10px;
        }
        .em{
            background-color: rgba(250, 235, 215, 0.637);
            width: 2em;
            font-size: 2em;
        }
        .rem{
            color: white;
            background-color: cornflowerblue;
            width: 2em;
            font-size: 2rem;
        }
```

Css function values

- The syntax always include the function name and paranthesis

<!-- rotate an element -->
- transform: rotate();
<!-- Calculate a computed value -->
- width: calc();
<!-- Embed an image to the backgroind of an element -->
- background-img: url();

ID's and in page linking

- can be used for CSS and in-page linking

```HTML
<a href = "#example">Link to spot on page</a>
<Section id="example">LInk</section>
```

## catagory of type faces

script - handwitten style
Decorative - ornamental have fake personility
monospace - each character uses the same amount of horizintal spaces
serif  - none for its decrative lines
sans serif

## float

Such as floating an image to have the text flow around it.

- float left
- float right

The majority of structural HTML elements used to create page layout are block level elements. So by default , they are displayed at full width and stack on top of each other

Flaot can be used to change the normal document flow by floating elements to the left and right side of the container
When element are floated they are removed by the normal flow they remain part of the flow


When there are no elements to apply a clear to, a self clearing techniques is applied to the parent.

1. Using overflow properties.

    ```HTML
    .parent
        .floated{...}
        .floated{...}
    ```

    ```CSS
    .floated{
        floa: left;
    }
    .parent{
        overflow: hidden;
        /* or */
        overflow: auto;
    }
    ```

    This is the comman techniques t slef clearing float.

2. Clearfix hack.

    Css snippet added to the parent of floated elements.

    ```HTML
    .clearfix
        p{floated element}
        p{floated element}
    ```

    ```CSS
    .clearfix{
        content: "";
        display: table;
        clear: both;
    }
    ```

3. display

    not currently supported in all browsers

    ```HTML
    .parent
        .floated{...}
        .floated{...}
    ```

    ```CSS
    .parent{
        display: flow-root;
    }
    ```

## Box model

...more soon

<iframe
    src="https://codepen.io/ullas_/pen/LYWywoG"
    style="width:100%; height:300px;">
</iframe>
