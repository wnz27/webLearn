# CSS
## Inline Styles
Although CSS is a different language than HTML, it's possible to write CSS code directly within HTML code using inline styles.
To style an HTML element, you can add the `style` attribute directly to the opening tag. After you add the attribute, you can set it equal to the CSS style(s) you'd like applied to that element.
```
<p style="color: red;">I'm learning to code!</p>
```
The code in the example above demonstrates how to use inline styling. The paragraph element has a `style` attribute within its opening tag. Next, the `style` attribute is set equal to `color: red;`, which will set the color of the paragraph text to red within the browser.
You might be wondering about the syntax of the following snippet of code: `color: red`;. At the moment, the details of the syntax are not important; you'll learn more about CSS syntax in other exercises. For now, it's important to know that inline styles are a quick way of directly styling an HTML element.
If you'd like to add more than one style with inline styles, simply keep adding to the `style` attribute. Make sure to end the styles with a semicolon (`;`).
`<p style="color: red; font-size: 20px;">I'm learning to code!</p>`

Q:

In index.html, use inline styles to set the font-family of the first paragraph to Arial.


## The <style> Tag
Inline styles are a fast way of styling HTML, but they also have limitations. If you wanted to style, for example, multiple `<h1>` elements, you would have to add inline styling to each element manually. In addition, you would also have to maintain the HTML code when additional `<h1>` elements are added.
Fortunately, HTML allows you to write CSS code in its own dedicated section with the `<style>` element. CSS can be written between opening and closing `<style>` tags. To use the `<style>` element, it must be placed inside of the `<head>` element.
```
<head>
  <style>
  </style>
</head>
```
After adding a `<style>` tag in the head section, you can begin writing CSS code.
```
<head>
  <style>
    p {
      color: red;
      font-size: 20px;
    }
  </style>
</head>
```
The CSS code in the example above changes the color of all paragraph text to red and also changes the size of the text to 20 pixels. Note how the syntax of the CSS code matches (for the most part) the syntax you used for inline styling. The main difference is that you can specify which elements to apply the styling to.
Again, the details of the CSS syntax in the example above aren't important at the moment. You will learn more about the details of CSS syntax in later lessons.
Q:
First, add a <style> element in the head of index.html. Then, make sure to delete the inline styles that you added to the paragraph.
Add the inline styles that you removed from the `<p>` element to the `<style>` element in the head.


## The .css file

Developers avoid mixing code by storing HTML and CSS code in separate files (HTML files contain only HTML code, 
and CSS files contain only CSS code).
You can create a CSS file by using the .css file name extension, like so: style.css

With a CSS file, you can write all the CSS code needed to style a page 
without sacrificing the readability and maintainability of your HTML file.

Q:
Take a look at index.html. Cut the CSS code in between the opening and closing <style> tags 
and paste it directly in the new file called style.css.
  
Make sure to delete the remaining <style> element (now empty) from index.html.


## Linking the CSS File
Perfect! We successfully separated structure (HTML) from styling (CSS), but the web page still looks bland. Why?

When HTML and CSS code are in separate files, the files must be linked. Otherwise, 
the HTML file won't be able to locate the CSS code, and the styling will not be applied.

You can use the `<link>` element to link HTML and CSS files together. 
The `<link>` element must be placed within the head of the HTML file. 
It is a self-closing tag and requires the following three attributes:

1. href — like the anchor element, the value of this attribute must be the address, or path, to the CSS file.

2. type — this attribute describes the type of document that you are linking to (in this case, a CSS file). 
The value of this attribute should be set to `text/css`.

3. rel — this attribute describes the relationship between the HTML file and the CSS file. 
Because you are linking to a stylesheet, the value should be set to stylesheet.

When linking an HTML file and a CSS file together, the `<link>` element will look like the following:

```
<link href="https://www.codecademy.com/stylesheets/style.css" type="text/css" rel="stylesheet">
```

Note that in the example above the path to the stylesheet is a URL:

`https://www.codecademy.com/stylesheets/style.css`

Specifying the path to the stylesheet using a URL is one way of linking a stylesheet.

If the CSS file is stored in the same [directory](https://en.wikipedia.org/wiki/Directory_(computing)) as your HTML file,
then you can specify a [relative path](https://en.wikipedia.org/wiki/Path_(computing)#Absolute_and_relative_paths) instead of a URL, like so:

`<link href="./style.css" type="text/css" rel="stylesheet">`

Using a relative path is very common way of linking a stylesheet.

Q:

1. Let's link the stylesheet style.css to the HTML file index.html.
First, add a `<link>` element within the `<head>` section.

2. Next, add the `href` attribute to the `<link>` element and set it equal to `style.css`.
Take a look at the web page in the browser to the right. Do you notice any changes?

3. Next, add the `type` attribute and set it to the correct value.

4. Finally, add the `rel` attribute and set it to the correct value.

## Tag Name
CSS can select HTML elements by using an element's tag name. 
A tag name is the word (or character) between HTML angle brackets.

For example, in HTML, the tag for a paragraph element is `<p>`. The CSS syntax for selecting `<p>` elements is:

```
p {
}
```

In the example above, all paragraph elements will be selected using a CSS selector. 
The selector in the example above is `p`. Note that the CSS selector matches the HTML tag for that element, 
but without the angle brackets.

In addition, two curly braces follow immediately after the selector (an opening and closing brace, respectively). 
Any CSS properties will go inside of the curly braces to style the selected elements.

Q:

1. In style.css, add a selector for `<h1>` elements.
Note: The content of the web page will update because we've already linked index.html and style.css for you.

2. Inside the curly braces of the `h1` selector you just declared, write:
`color: maroon;`
This code will make the text color of all `<h1>` tags maroon.

## Class Name
CSS is not limited to selecting elements by tag name. HTML elements can have more than just a tag name; 
they can also have attributes. One common attribute is the `class` attribute. 
It's also possible to select an element by its `class` attribute.

For example, consider the following HTML:

`<p class="brand">Sole Shoe Company</p>`

The paragraph element in the example above has a `class` attribute within the `<p>` tag. 
The `class` attribute is set to `"brand"`. To select this element using CSS, 
we could use the following CSS selector:

```
.brand {
}
```

To select an HTML element by its class using CSS, a period (`.`) must be prepended to the class's name. 
In the example above case, the class is `brand`, so the CSS selector for it is `.brand`.

Q:

1. In *style.css*, add a CSS selector for the HTML element with a class of `title`.

2. Inside the curly braces of the `.title` selector you just declared, write:
`color: teal;`
This code will change the color of the title to teal, since the title `h1` element has a class of `title` in the HTML. 
You can see the HTML element by navigating to index.html on line 11.
We'll see in a later exercise why using `.title` overrides the `h1` selector.


## Multiple Classes
We can use CSS to select an HTML element's `class` attribute by name.

So far, we've selected elements using only one class name per element. 
If every HTML element had a single class, all the style information for each element would require a new class.

Luckily, it's possible to add more than one `class` name to an HTML element's class attribute.

For instance, perhaps there's a heading element that needs to be green and bold. You could write two CSS rules like so:

```
.green {
  color: green;
}
.bold {
  font-weight: bold;
}
```

Then, you could include both of these classes on one HTML element like this:

`<h1 class="green bold"> ... </h1>`

We can add multiple classes to an HTML element's `class` attribute by separating them with a space. 
This enables us to mix and match CSS classes to create many unique styles without writing a custom class for every style combination needed.

Q:

1. In *style.css*, add a class selector that will make the title of the page stand out more by making all of its letters uppercased. 
Write a class named `.uppercase`. Then, write this inside of its curly braces:

`text-transform: uppercase;`

2. Now you can add the class to the title element. Navigate to index.html. 
On line 11, there is a `<h1>` element that has a class of `title`. 
Add the `uppercase` class to this element.


## ID Name
If an HTML element needs to be styled uniquely (no matter what classes are applied to the element), 
we can add an ID to the element. To add an ID to an element, the element needs an `id` attribute:

`<h1 id="large-title"> ... </h1>`

Then, CSS can select HTML elements by their `id` attribute. To select an `id` element, 
CSS prepends the `id` name with a hashtag (`#`). For instance, 
if we wanted to select the HTML element in the example above, it would look like this:

```
#large-title {
}
```

The `id` name is `large-title`, therefore the CSS selector for it is `#large-title`.

Q:

1. In *style.css*, add a CSS selector for an element with an `id` of `article-title`. Inside of its curly braces, write:

```
font-family: cursive;
text-transform: capitalize;
```

These two CSS attributes will make the font cursive and will capitalize the first letter of each word, 
while lowercasing the rest.

2. Navigate to index.html. On line 11, add an `id` attribute to the `h1` element, 
and include `article-title` as its `id`. 
You'll see the title change to a cursive font that is not all uppercased.









