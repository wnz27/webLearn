# CSS

---

# Selector

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


## Classes and IDs
CSS can select HTML elements by their tag, class, and ID. 
CSS classes and IDs have different purposes, which can affect which one you use to style HTML elements.

CSS classes are meant to be reused over many elements. 
By writing CSS classes, you can style elements in a variety of ways by mixing classes on HTML elements.

For instance, imagine a page with two headlines. 
One headline needs to be bold and blue, and the other needs to be bold and green. 
Instead of writing separate CSS rules for each headline that repeat each other's code, 
it's better to write a .bold CSS rule, a `.green` CSS rule, and a `.blue` CSS rule. 
Then you can give one headline the `bold green` classes, and the other the `bold blue` classes.

While classes are meant to be used many times, an *ID is meant to style only one element*. 
As we'll learn in the next exercise, IDs override the styles of tags and classes. 
Since IDs override class and tag styles, they should be used sparingly and only on elements that need to always appear the same.

1. On line 13 of *index.html*, there’s an element that displays the time the article on the page was published.
Add a class attribute, with a class of `publish-time`.

2. Add a `publish-time` class selector in *style.css* and make its text color `gray` by writing this within the CSS rule’s body:
`color: gray;`


## Specificity
Specificity is the order by which the browser decides which CSS styles will be displayed. 
A best practice in CSS is to style elements while using the lowest degree of specificity, 
so that if an element needs a new style, it is easy to override.
IDs are the most specific selector in CSS, followed by classes, and finally, tags. 
For example, consider the following HTML and CSS:

`<h1 class="headline">Breaking News</h1>`

```
h1 {
  color: red;
}
.headline {
  color: firebrick;
}
```

In the example code above, the color of the heading would be set to `firebrick`, 
as *the class selector is more specific than the tag selector.*
If an ID attribute (and selector) were added to the code above, 
the styles within the ID selector's body would override all other styles for the heading. 
*The only way to override an ID is to add another ID with additional styling.*
Over time, as files grow with code, many elements may have IDs, 
which can make CSS difficult to edit, since a new, more specific style must be created to change the style of an element.
To make styles easy to edit, it's best to style with a tag selector, if possible. 
If not, add a class selector. If that is not specific enough, then consider using an ID selector.

Q:

1. In *index.html*, the element on line 11 has an `h1` tag, two classes, and an ID. 
Since the ID is more specific than both, its styles will be applied to the element. 
Let's re-write the ID of this element to be less specific by creating classes.
In *index.html*, delete the `id` attribute on the `h1` element on line 11.

2. Now delete the `#article-title` ID in the CSS.
Navigate to *style.css* delete the `#article-id` ID selector and its contents.

3. Navigate to *style.css*. Add a class selector named `.cursive`. Inside its body, write:
`font-family: cursive;`

4. Add another class selector named `.capitalize`. In its curly braces, write:
`text-transform: capitalize;`

5. Now, navigate back to *index.html*, and replace the `uppercase` class with 
the `cursive` and `capitalize` classes on the `h1` element on line 11.


## Chaining Selectors
When writing CSS rules, it's possible to require an HTML element to have two or more CSS selectors at the same time.
This is done by combining multiple selectors, which we will refer to as chaining. 
For instance, if there was a `.special` class for `h1` elements, the CSS would look like:

```
h1.special {
}
```

The code above would select only the `h1` elements that have a class of `special`. 
If a `p` element also had a class of `special`, the rule in the example would not style the paragraph.

Q：

Let's use chaining to select the destinations to add a style to them.
In *style.css*, write a CSS selector for `h2` elements with a class of `.destination`. 
Inside the selector's curly braces, write this:
`font-family: cursive;`
This will make the destinations cursive, like the title of the article.

## Nested Elements
In addition to chaining selectors to select elements, 
CSS also supports selecting elements that are nested within other HTML elements. 
For instance, consider the following HTML:

```
<ul class='main-list'>
  <li> ... </li>
  <li> ... </li>
  <li> ... </li>
</ul>
```

The nested `<li>` elements are selected with the following CSS:

```
.main-list li {
}
```

In the example above, `.main-list` selects the `.main-list` element (the unordered list element). 
The nested `<li>` are selected by adding `li` to the selector, separated by a space, 
resulting in `.main-list li` as the final selector *(note the space in the selector).*
Selecting elements in this way can make our selectors even more specific 
by making sure they appear in the context we expect.

Q:

1. In *index.html*, each destination has a description paragraph below it. 
Inside each description, there's a list of attractions. 
Let’s select the `Top Attractions` element and make it stand out more by making it teal.
Navigate to *style.css*. Add a selector that targets all of the `h5` elements 
nested inside elements with class `.description`.

2. Inside the curly braces of the selector, write:
`color: teal;`


## Chaining and Specificity

In the last exercise, instead of selecting all `h5` elements, you selected only the `h5` elements nested inside the `.description` elements. 
This CSS selector was more specific than writing only `h5`. 
Adding more than one tag, class, or ID to a CSS selector increases the specificity of the CSS selector.

For instance, consider the following CSS:

```
p {
  color: blue;
}
.main p {
  color: red;
}
```

Both of these CSS rules define what a `p` element should look like. 
Since `.main p` has a class and a `p` tag as its selector, only the `p` elements inside the `.main` element will appear `red`. 
This occurs despite there being another more general rule that states `p` elements should be `blue`.

Q:
In *style.css*, write a selector for `h5` elements. Inside of the curly braces write:
`color: rebeccapurple;`

Notice that the `h5` elements in the descriptions will not change color. They will continue to be `teal`.
This is due to there being a more specific selector for `h5` elements that you wrote in the last exercise. 
Because of the more specific CSS selector (`.description h5`), the more general selector of `h5` will not take hold.


## Important
There is one thing that is even more specific than IDs: `!important`. 
`!important` can be applied to specific attributes instead of full rules. 
It will override any style no matter how specific it is. 
As a result, it should almost never be used. 
Once `!important` is used, it is very hard to override.
The syntax of `!important` in CSS looks like this:

```
p {
  color: blue !important;
}
.main p {
  color: red;
}
```

Since `!important` is used on the `p` selector’s `color` attribute, all `p` elements will appear `blue`, 
even though there is a more specific `.main p` selector that sets the `color` attribute to `red`.
The `!important` flag is only useful when an element appears the same way 100% of the time. 
Since it's almost impossible to guarantee that this will be true throughout a project and over time, 
it's best to avoid `!important `altogether. 
If you ever see `!important` used (or are ever tempted to use it yourself) we strongly recommend reorganizing your CSS.
Making your CSS more flexible will typically fix the immediate problem and make your code more maintainable in the long run.

Q:

Add `!important` to the `h5` selector's `color` attribute that you defined in the last exercise. 
`!important` should go after `rebeccapurple`, and before the semicolon.
Notice that the `h5` elements will now be `rebeccapurple` instead of `teal`. 
That's because `!important` will override any other style no matter what.


## Multiple Selectors
In order to make CSS more concise, it's possible to add CSS styles to multiple CSS selectors all at once. 
This prevents writing repetitive code.

For instance, the following code has repetitive style attributes:

```
h1 {
  font-family: Georgia;
}
.menu {
  font-family: Georgia;
}
```

Instead of writing `font-family: Georgia` twice for two selectors, 
we can separate the selectors by a comma to apply the same style to both, like this:

```
h1, 
.menu {
  font-family: Georgia;
}
```

By separating the CSS selectors with a comma, both the `h1` and the `.menu` elements will receive the `font-family: Georgia` styling.

Q:

Write selectors for the `h5` and `p` elements so they both will be styled with the same CSS rule. 
Apply this style to both elements:
`font-family: Georgia;`
Notice that the font across the page will change to `Georgia` without writing the same CSS rule twice.


## Review CSS Selectors
Throughout this lesson, you learned how to select HTML elements with CSS and apply styles to them. 
Let's review what you learned:

* CSS can change the look of HTML elements. In order to do this, CSS must select HTML elements, then apply styles to them.
* CSS can select HTML elements by tag, class, or ID.
* Multiple CSS classes can be applied to one HTML element.
* Classes can be reusable, while IDs can only be used once.
* IDs are more specific than classes, and classes are more specific than tags. 
That means IDs will override any styles from a class, and classes will override any styles from a tag selector.
* Multiple selectors can be chained together to select an element. This raises the specificity, but can be necessary.
* Nested elements can be selected by separating selectors with a space.
* The `!important` flag will override any style, however it should almost never be used, 
as it is extremely difficult to override.
* Multiple unrelated selectors can receive the same styles by separating the selector names with commas.
Great work this lesson. With this knowledge, you'll be able to use CSS to change the look 
and feel of websites to make them look great.

Index.html:

```
<!DOCTYPE html>
<html>
<head>
  <title>Vacation World</title>
  <link href="css_test.css" type="text/css" rel="stylesheet">
</head>
<body>
  <img src="https://s3.amazonaws.com/codecademy-content/courses/freelance-1/unit-2/explorer.jpeg" />
  <h1 class="title cursive capitalize">Top Vacation Spots</h1>
  <h5>By: Stacy Gray</h5>
  <h6 class="publish-time">Published: 2 Days Ago</h6>
  <p>The world is full of fascinating places. Planning the perfect vacation involves packing up, leaving home, and experiencing something new.</p>
  <h2 class="destination">1. Florence, Italy</h2>
  <div class="description">A city-size shrine to the Renaissance, Florence offers frescoes, sculptures, churches, palaces, and other monuments from the richest cultural flowering the world has known. Names from its dazzling historical pastDante, Michelangelo, Galileo, Machiavelliare some of the most resonant of the medieval age. <a href="http://travel.nationalgeographic.com/travel/city-guides/florence-italy/" target="_blank">Learn More</a>.
    <h5>Top Attractions</h5>
    <ul>
      <li>Museums</li>
      <li>Bike Tours</li>
      <li>Historical Monuments</li>
    </ul>
  </div>
  <h2 class="destination">2. Beijing, China</h2>
  <div class="description">A city in the midst of reinventing itself and continuing to build on the success of the 2008 Summer Olympics, Beijing is a place of frenzied construction. New housing, new roads, and new sports venues seem to spring up overnight. At the same time, the capital of the Peoples Republic of China remains an epicenter of tradition, with the treasures of nearly 2,000 years as the imperial capital still on viewin the famed Forbidden City and in the luxuriant pavilions and gardens of the Summer Palace.
    <a href="http://travel.nationalgeographic.com/travel/city-guides/beijing-china/" target="_blank">Learn More</a>.
    <h5>Top Attractions</h5>
    <ul>
      <li>Biking</li>
      <li>Historical Sites</li>
      <li>Restaurants and Dining</li>
    </ul>
  </div>
  <h2 class="destination">3. Seoul, South Korea</h2>
  <div class="description">The Korean capital is a city of contrasts. Fourteenth-century city gates squat in the shadow of 21st-century skyscrapers, while the broad Han River is back-dropped by granite mountains rising in the city centercomplete with alpine highways speeding around their contours and temples nestling among their crags. Fashionable, gadget-laden youths battle for sidewalk space with fortune-tellers and peddlers, while tiny neighborhoods of traditional cottages contrast with endless ranks of identical apartments.
    <a href="http://travel.nationalgeographic.com/travel/city-guides/seoul-south-korea/" target="_blank">Learn More</a>.
    <h5>Top Attractions</h5>
    <ul>
      <li>Parasailing</li>
      <li>Segway Tours</li>
      <li>Spas and Resorts</li>
    </ul>
  </div>
  <h2> More Desinations </h2>
  <ul>
    <li><h4 class="destination">Jackson Hole, Wyoming</h4></li>
    <li><h4 class="destination">Cape Town, South Africa</h4></li>
    <li><h4 class="destination">La Paz, Bolivia</h4></li>
  </ul>
  <p>&mdash;Best of luck with your travels, and be sure to send pictures and stories. We"d love to hear them!</p>
</body>
</html>
```

Style.css:

```
p {
    color: blue;
    font-family : Arial;
}
h1 {
    color: maroon;
}
.title {
    color: tomato;
}
.uppercase{
    text-transform: uppercase;
}

.publish-time {
    color: gray;
}
.cursive {
    font-family: cursive;
}
.capitalize {
    text-transform: capitalize;
}
h2.destination {
    font-family: cursive;
}
.description h5{
    color: teal;
}
p,
h5 {
    color: rebeccapurple !important;
    font-family: Georgia;
}
```

---

# Visual Rules

## Introduction To Visual Rules
In this lesson, you'll learn the basic structure and syntax of CSS so that you can start styling web page elements.
Explore the code to the below. Think about how it relates to the web page on the right side of the browser.
Index.html:

```
<!DOCTYPE html>
<html>
<head>
  <title>The Rise of Soccer in The US</title>
  <link href="style.css" type="text/css" rel="stylesheet">
</head>
<body>
  <div class="content">
    <img src="https://s3.amazonaws.com/codecademy-content/courses/web-101/unit-4/htmlcss1-img_writer-avatar.jpg" class="writer-img">
    <h3 class="byline">Article By: Jane Dover</h3>
    <h1>How the Rise of Soccer in the US Is Changing the Face of Youth Sports</h1>
    <h2>The focus on soccer in youth sports programs is exploding nation-wide</h2>
    <p>When the first World Cup arrived in the US in the 90's everyone officially declared that soccer was it. Well it's taken it's time but we can definitely see the influence of soccer, especially women's soccer, across the US. This year, 3 million kids
      played in youth soccer leagues with 2/3 of those leagues for girls. In fact, in the 12-17 age range the MLS has surpassed the MLB and NFL in popularity.</p>
    <p>Part of this meteoric rise can be attributed to the impressively soaring ad dollars being pumped into the Women's World Cup games in 2014. The women's games generated $40 million for Fox, that's definitely not chump change. And those advertisers,
      like ATT, Coca Cola, Verizon, Nike, Visa, and other heavy hitters, are working to make sure they see those numbers grow year after year by investing in youth soccer facilities and promoting programs across the country. </p>
    <p>Now that big business is involved you can be assured you'll see a continued rise in popularity in soccer across the country for years to come. </p>
  </div>
  <div class="image">
    <p class="caption">The local semi- pro soccer team in Seattle, WA plays an international friendly</p>
  </div>
</body>
</html>
```

Style.css:

```
body {
  /* Old browsers */
  background: #141E30;
  /* Chrome 10-25, Safari 5.1-6 */
  background: -webkit-linear-gradient(-45deg, #35577D, #141E30);
  /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  background: linear-gradient(-45deg, #35577D, #141E30);
  margin: 0;
  padding: 0;
}

h1 {
  color: #FFF;
  font-size: 2em;
  padding-top: 100px;
  width: 100%;
}

h2 {
  border-bottom: 1px solid rgba(255, 255, 255, 0.5);
  color: rgba(255, 255, 255, 0.5);
  font-weight: 100;
  font-size: 22px;
  line-height: 24px;
  padding-bottom: 30px;
  text-align: left;
  width: 70%;
}

p {
  color: AliceBlue;
  line-height: 1.3em;
  text-align: left;
  width: 100%;
}

.byline {
  font-family: Helvetica;
  color: rgba(255, 255, 255, 0.5);
  float: left;
  font-size: 14px;
  padding-left: 10px;
  text-transform: uppercase;
}

.caption {
  display: block;
  font-family: 'Playfair Display', serif;
  font-size: 14px;
  font-style: italic;
  line-height: 14px;
  margin-left: 20px;
  padding: 10px;
  position: relative;
  top: 80%;
  width: 60%;
}

.content {
  padding: 40px;
}

.image {
  background-image: url("https://s3.amazonaws.com/codecademy-content/courses/web-101/unit-4/htmlcss1-img_soccer.jpeg");
  background-size: cover;
  background-position: center;
  height: 300px;
}

.writer-img {
  -webkit-box-shadow: 5px 0px 5px 0px rgba(0, 0, 50, 0.97);
  -moz-box-shadow: 5px 0px 5px 0px rgba(0, 0, 50, 0.97);
  box-shadow: 5px 0px 5px 0px rgba(0, 0, 50, 0.97);
  float: left;
  width: 50px;
}
```

## CSS Structure

To style an HTML element using CSS, you need to write a CSS declaration inside the body of a CSS selector.

```
h1 {
  color: blue;
}
```

The example above selects the `<h1>` element. Inside of the selector's body, we typed `color: blue`. 
This line is referred to as a CSS declaration. CSS declarations consist of a property and a value.
Property — the property you'd like to style of that element (i.e., size, color, etc.).
Value — the value of the property (i.e., 18px for size, blue for color, etc.).
In the example above, the property is `color` and the value is `blue`. 
Note that a semicolon (`;`) is always used at the end of a declaration.
Finally, the entire snippet of code in the example above is known as a CSS rule. 
A CSS rule consists of the selector (here, `h1`) and all declarations inside of the selector.

Instructions
Look at *style.css* and explore the different CSS rule sets.


## Font Family
If you've ever used a formatted word processor, chances are that you probably also used a feature 
that allowed you change the font you were typing in. 
Font refers to the technical term [typeface](https://en.wikipedia.org/wiki/Typeface), or font family.

To change the typeface of text on your web page, you can use the `font-family` property.

```
h1 {
  font-family: Garamond;
}
```

In the example above, the font family for all main heading elements has been set to `Garamond`.
When setting typefaces on a web page, keep the following points in mind:

1. The font specified in a stylesheet must be installed on a user's computer 
in order for that font to display when a user visits the web page.

2. The default typeface for all HTML elements is `Times New Roman`. 
You may be familiar with this typeface if you have ever used a formatted word processor. 
If no `font-family` attribute is defined, the page will appear in `Times New Roman`.

3. It's a good practice to limit the number of typefaces used on a web page to 2 or 3. 
This helps the page load faster in some cases and is usually a good design decision.

4. When the name of a typeface consists of more than one word, 
it's a best practice to enclose the typeface's name in quotes, like so:

```
h1 {
  font-family: "Courier New";
}
```

You can find a reference of web safe fonts [here](https://www.cssfontstack.com/).

Q：
1. Inside *style.css*, add the font family of the main heading (`h1`) and subheading (`h2`) to `Georgia`.

2. Next, change the font family of the paragraph to `Helvetica`.

## Font Size
Changing the typeface isn't the only way to customize text. Often times, 
different sections of a web page are highlighted by modifying the font size.
To change the size of text on your web page, you can use the `font-size` property.

```
p {
  font-size: 18px;
}
```

In the example above, the `font-size` of all paragraphs was set to `18px`. 
`p`x means pixels and is a way to measure font size.

Q:
In *style.css*, set the `font-size` of paragraph elements to 18 pixels.

## Font Weight
In CSS, the `font-weight` property controls how bold or thin text appears.

```
p {
  font-weight: bold;
}
```

In the example above, all paragraphs on the web page would appear bolded.
The `font-weigh`t property has a another value: `normal`. Why does it exist?
If we wanted all text on a web page to appear bolded, we could select all text elements 
and change their font weight to `bold`. If a certain section of text was required to appear normal, 
however, we could set the font weight of that particular element to `normal`, 
essentially shutting off bold for that element.
Q:
In *style.css*, set the font weight of paragraph elements to `bold`.


## Text Align
No matter how much styling is applied to text (typeface, size, weight, etc.), 
text always appears on the left side of the browser.
To align text we can use the `text-align` property. 
The `text-align` property will align text to the element that holds it, otherwise known as its parent.

```
h1 {
  text-align: right;
}
```

The `text-align` property can be set to one of the following three values:

`left` — aligns text to the left hand side of its parent element, which in this case is the browser.

`center `— centers text inside of its parent element.

`right` — aligns text to the right hand side of its parent element.
Q:
In *style.css*, set the `text-align` property of the main heading so that it appears in the center.









