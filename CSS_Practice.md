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
