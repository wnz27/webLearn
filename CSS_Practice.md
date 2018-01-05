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





