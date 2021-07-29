# HTML

HTML `Hypertext markup language` is the primary building block for building Front end.

CSS is important because it controls all design-related aspects of your website like `Typography`, `colours`, `page layouts`, `Responsive design` and any other visual aspects of your website are all controlled by CSS.

## HTML Elements

```html
    <h1>First Heading</h1>
```

As you can see:

- `<h1>` - The Opening heading tag

- `First Heading` - The Content

- `</h1>` - The Closing tag

Each part of a web page, such as a paragraph, an image, a link or anything else you can interact with, is an element. Each elements has its own behaviour.

It consists of `Opening tag`, `The content`, `The closing tag`

```doc
The HTML element is everything from the <start tag> to the </end tag>:
```

## HTML Tags

Tag is used for creating an element they helpful for web browser to distinguish between an HTML content and a simple content.

rules:

- HTML tags must enclosed within the angle brackets < > .
- If you open the tag you must close it (`except: selfclosing tag`)
- There are some HTML elements that don't have a closing tag or any contents. These are called void elements. Void
elements include `<img>`, `<meta>`, `<link>` and `<input>`.

```doc
    Tags begin or end an element in source code, whereas elements are part of the DOM, the document model for displaying the page in the browser.
```

## HTML Structure

Let take an example and slice it up!

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- This's a comment -->
    <h1>Heading level 1</h1>
    <p>The p element represents a paragraph.</p>
</body>
</html>
```

![as](/img/html-structure.png)

- At the top we have 🗎:

    `<!DOCTYPE html>` => This help the browser to understand the version of HTML used in the document this is `HTML5 document`

- Inside that we have root 🖺:

    `<html>` => This is the container of all the HTML content, act as a `root of the document`

- Inside the root we have The invisibler:

    `<head>` => This contains the **meta data** of the HTML (essential information) && `invisible to the visitor` 🦸.

    Meta-data includes `charset attribute` which is used by the browser to know the character set used in the page [By default its set to UTF-8 ]

    We also have `<title>` The title of the page, displayed on the tab of the browser

- Inside the root next to head:

    `<body>` tag contain the content that is visible to the user when they visit a page

    Inside the `body` tag we have all the other tag which is used to structure the web page
    example: `<h1>`, `<p>`, `<header>`, `<section>`, `<div>`, ...

    ```note
    **!if you open the tag you must close it (except: self-closing tag)**
    ```

## Headings Tags

- There are `six level` separate header tags to indicate headings of various sizes and thicknesses.

- Enumerated as `heading 1` through `heading 6`,

- `Heading 1 has the largest and thickest` text while `heading 6 is the smallest and thinnest`, down to the paragraph level.

```html
<h1>Heading 1</h1>

<h2>Heading 2</h2>

<h3>Heading 3</h3>

<h4>Heading 4</h4>

<h5>Heading 5</h5>

<h6>Heading 6</h6>
```

>! Search engines and other user agents usually index page content based on heading elements, for example to create a table of contents, so using the correct structure for headings is important.

## Paragraphs Tag

In html for paragraph we use `<p>` tag

for example:

```html
    <p>Some species live in houses where they hunt insects attracted by artificial light.</p>
```

![as](/img/p-tag.png)

## Text Formatting

HTML also provides in-text formatting tags to apply specific
text-related styles to portions of text

- Mark Tag

    ```html
    <mark> element </mark>
    ```

    The <mark>mark tag</mark> is new in HTML5 is used to mark or highlight text in a document

- Bold Text

    ```html
    use the <strong> strong tag </strong>
    use the <b> b tag </b>
    ```

    To bold text, use the <strong> strong </strong> or else <b> b (bold) </b> tag:

- Italic Text

    ```html
    use the <em> string tag </em>
    use the <i> b tag </i>
    ```

    To italicize text, use the <em> em </em> or else <i> i </i> tag:

- Underlined Text

    ```html
    While the <u> element itself was deprecated </u> in HTMl 4, it was reintroduced with alternate semantic meaning in
    HTML 5 
    ```

    While the <u> element itself was deprecated </u> in HTMl 4, it was reintroduced with alternate semantic meaning in HTML 5

- Quotations

    ```html
    <blockquote>
        <h1>OMG a heading!</h1>
        <ul>
            <li>Block quotes can contain more than just paragraphs…</li>
        </ul>
    </blockquote>
    ```

    ![blockquote](/img/blockquote.png)

    The HTML `<blockquote>` tag is used for indicating long quotations (i.e. quotations that span multiple lines).

## HTML anchors and attributes

### Anchor tag

`<a>` tag is used to create an element (anchor element) which represent `hyperlink` & the important part is the `href` attribute which point's to the destination

By default, links will appear as follows in all browsers:

- An unvisited link is underlined and blue
- A visited link is underlined and purple
- An active link is underlined and red

```html
<a href="https://github.com/ullaskunder3">GitHub Profile</a>
```

![blockquote](/img/anchor-tag.png)

Attrubutes of anchor tag

| Attribute | Value                        | Description                           |
|-----------|------------------------------|---------------------------------------|
| href      | URL                          | Link Destination or a page using url  |
|           |                              |                                       |
| target    | _blank,                      |                                       |
|           | _self,                       |                                       |
|           | _parent,                     |                                       |
|           | _top                         | Where to open the link doc            |
|           |                              |                                       |
| download  | filename                     | Target link to download when clicked  |
|

...there are more but 🥱

## HTML5 tags

- `section`: This tag represents a generic standalone section of a document.  Sections should always have a heading, with very few exceptions.

    ![section tag](/img/section-tag.png)

- `article`: This tag represents an independent piece of content of a document, such as a blog entry or newspaper article.

    ![section tag](/img/article.png)

- `aside`: This tag represents a piece of content that is only slightly related to the rest of the page.

    ![section tag](/img/aside-tag.png)

- `header`: This tag represents the header of a section.

- `footer`: This tag represents a footer for a section and can contain information about the author, copyright information, et cetera.

- `nav`: This tag represents a section of the document intended for navigation.

- `<div>`: HTML element is the generic container for flow content

it's all look 😕 ==> just wait for CSS 🤩

## Lists

HTML offers three ways for specifying lists: `ordered lists`, `unordered lists`, and `description lists`.

### Ordered list

- An ordered list can be created with the `<ol>` tag and each list item can be created with the `<li>` tag.

```html
<ol>
    <li>Iron man</li>
    <li>Vision</li>
    <li>Caption America</li>
    <li>Thor</li>
    <li>Loki</li>
</ol>
```

![order list](/img/order-tag.png)

We can manually changing the numbers 😁

```html
<ol start= "5">
    <li>Iron man</li>
    <li>Vision</li>
    <li>Caption America</li>
    <li>Thor</li>
    <li>Loki</li>
</ol>
```

![order list](/img/order-tag1.png)

### Unordered list

- An unordered list can be created with the `<ul>` tag and each list item can be created with the `<li>` tag

![unorder list](/img/unorder-tag.png)

### Nesting lists

We can nest lists to represent sub-items of a list item.

![nesting list](/img/nesting-li.png)

### Description List

- Description list can be created with the `dl` element.

- It consists of `name-value groups`, where the `name is given in the dt element`, and the `value is given in the dd element`.
( definition list called before HTML5 )

![description list](/img/dl-tag.png)

## Tables

`<table>` element allows web developer to display tabular data in two dimensional table with rows and columns of cells.

```html
<table>
    <tr>
        <th>Heading 1/Column 1</th>
        <th>Heading 2/Column 2</th>
    </tr>
    <tr>
        <td>Row 1 Data Column 1</td>
        <td>Row 1 Data Column 2</td>
    </tr>
    <tr>
        <td>Row 2 Data Column 1</td>
        <td>Row 2 Data Column 2</td>
    </tr>
</table>
```

![table](/img/table-tag.png)

There are attribute which is used to span multiple column or rows...

- These attributes can be applied to `<th>` and `<td>` elements.

![table span](/img/col-row-span.png)

## HTML Comments

HTML comments can be used to leave notes to yourself or other developers about a specific point in code. They can be initiated with `<!-- and concluded with -->`