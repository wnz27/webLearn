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

2. Next, add the href attribute to the `<link>` element and set it equal to style.css.
Take a look at the web page in the browser to the right. Do you notice any changes?

3. Next, add the type attribute and set it to the correct value.

4. Finally, add the `rel` attribute and set it to the correct value.



