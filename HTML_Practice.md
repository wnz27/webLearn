# HTML

## What is HTML?
HTML is the language used to create the websites you visit everyday. It provides a logical way to structure content for websites.
Let's analyze the acronym "HTML," as it contains a lot of useful information. HTML stands for HyperText Markup Language.
A markup language is a computer language that defines the structure and presentation of raw text. Markup languages work by surrounding raw text with information the computer can interpret, "marking it up" to be processed.
In HTML, the computer can interpret raw text that is wrapped in HTML elements. These elements are often nested inside one another, with each containing information about the type and structure of the information to be displayed in the browser.
HyperText is text displayed on a computer or device that provides access to other text through links, also known as “hyperlinks.” In fact, you probably clicked on many, many hyperlinks on your path to this Codecademy course!
Q:
In the code editor to the right, type your name in between `<h1> and </h1>`, then press Run.
`<h1>27</h1>`


## !DOCTYPE
Whether you realize it or not, when you read text, your brain must first identify the text's language. If you can understand that language, then your brain immediately begins to interpret the text. This same process happens whether you're reading a street sign, a book, or a name tag.
Web browsers work in a similar way. They must know what language a document is written in before they can process its contents.
You can let web browsers know that you are using HTML by starting your document with a document type declaration.
The declaration looks like this: <!DOCTYPE html>. This declaration is an instruction. It tells the browser what type of document to expect, along with what version of HTML is being used in the document.
<!DOCTYPE html> must be the first line of code in all of your HTML documents. If you don't use the declaration, your HTML code will likely still work, however, it's risky. For now, the browser will correctly assume that the html in <!DOCTYPE html> is referring to HTML5, as it is the current standard.
In the future, however, a new standard will override HTML5. Future browsers may assume you're using a different, newer standard, in which case your document will be interpreted incorrectly. To make sure your document is forever interpreted correctly, always include <!DOCTYPE html> at the very beginning of your HTML documents.
`<!DOCTYPE html>`


## Preparing for HTML
Great! Browsers that read your code will know to expect HTML when they attempt to read your file.
The <!DOCTYPE html> declaration is only the beginning, however. It indicates to the browser that you will use HTML in the document, but it doesn't actually add any HTML structure or content.
To create HTML structure and content, we must add opening and closing <html> tags, like so:
```
<!DOCTYPE html>
<html>
</html>
```
Anything between the opening <html> and closing </html> tags will be interpreted as HTML code. Without these tags, it's possible that browsers could incorrectly interpret your HTML code.


## HTML Anatomy
Before we move forward, it's important that we discuss how HTML elements are structured. The diagram to the right displays an HTML paragraph element.
In this example, the paragraph element is made up of one opening tag` (<p>)`, the “Hello world!” text, and a closing tag `(</p>)`:
Let's quickly review each part of the tag pictured:
1. HTML Tag - The element name, surrounded by an opening (<) and closing (>) angle bracket.
2. HTML element (or simply, element) - a unit of content in an HTML document formed by HTML tags and the text or media it contains.
3. Opening tag - the first HTML tag used to start an HTML element. The tag type is surrounded by opening and closing angle brackets.
4. Element content - The information (text or other elements) contained between the opening and closing tags of an HTML element.
5. Closing tag - the second HTML tag used to end an HTML element. Closing tags have a forward slash (/) inside of them, directly after the left angle bracket.

Most elements require both opening and closing tags, but some call for a single self-closing tag. We'll encounter examples of both element types in the next few exercises.
![](https://github.com/wnz27/webLearn/blob/master/Web_Image/HTML_element.png)


## The Head
So far you've done two things:
Declared to the browser that your code is HTML.
Added the HTML element (<html>) that will contain the rest of your code.
Let's also give the browser some information about the page. We can do this by adding a <head> element.
The <head> element contains the metadata for a web page. 
Metadata is information about the page that isn't displayed directly on the web page.
You'll see an example of this in the next exercise.
The opening and closing head tags (<head></head>) typically appear as the first item after your first HTML tag.
```
<!DOCTYPE html>
<html>
  <head></head>
</html>
```


## Page Titles
What kind of metadata about the web page can the <head> element contain?
If you navigate to the Codecademy catalog and look at the top of your browser (or at the tab you have open), 
you'll notice the words `All Courses | Learn to code interactively | Codecademy`, which is the title of the web page.
The browser displays the title of the page because the title can be specified directly inside of the <head> element, 
by using a <title> tag.
```
<!DOCTYPE html>
<html>
  <head>
    <title>My Coding Journal</title>
  </head>
</html>
```
If we were to open a file containing the HTML code in the example above, 
the browser would display the words My Coding Journal in the title bar (or in the tab's title).
Q:
Add a title to your web page using the <title> element. The title can be anything you'd like.
Unfortunately, you won't be able to see the title of your page in the smaller browser to the right. 
We'll show you what it would look like in the next exercise.
```
<html>
  <head>
    <title>My title</title>
  </head>
</html>
```


## Where Does the Title Appear?
Good work! If the browser within the environment had a title bar,
you'd see the title of the web page you added where it appears in the image to the right.
![](https://github.com/wnz27/webLearn/blob/master/Web_Image/Site_Title.png)



## The Body
We've added some HTML, but still haven't seen any results in the web browser to the right. Why is that?
Before we can add content that a browser will display, we have to add a body to the HTML file. Only content inside the opening and closing body tags can be displayed to the screen.
Once the file has a body, many different types of content – including text, images, and buttons – can be added to the body.
```
<!DOCTYPE html>
<html>
  <head>
    <title>I'm Learning To Code!</title>
  </head>
  <body>
  </body>
</html>
```
In the example above, the opening body tag (<body>) is placed directly below the closing head tag (</head>), and the closing body tag (</body>) is placed directly above the closing html tag (</html>).
Q:
1. Add a body to your web page using the <body> element.
2. Add the following code between your opening and closing body tags.
```
<p>Shall I compare thee to a summer's day? Thou art more lovely and more temperate</p>
```
```
<!DOCTYPE html>
<html>
  <head>
    <title>My Coding Journey</title>
  </head>  
  <body>
    <p>Shall I compare thee to a summer's day? Thou art more lovely 	and more temperate</p>
  </body>
</html>
```


## Self-closing Tag
Thus far we have only seen HTML elements with an opening and a closing tag. A few types of elements, however, require only one tag.
Self-closing elements contain all the information the browser needs to render the element inside a single tag. Also, because they are single tags, they cannot wrap around raw text or other elements.
The line break element `<br />` is one example of a self-closing tag. You can use it anywhere within your HTML code. The result is a line break in the browser.
`<p>line one<br />line two</p>`
In the example above, the paragraph tags `(<p>)` enclose two phrases, split by a break tag `(<br />)`. Note that single tags, unlike elements with two tags, can't wrap around raw text or other elements.
The code in the example above will result in an output that looks like the following:
```
line one
line two
```
Without the break tag, the browser would render line one and line two on the same line.
Q:
Add a self-closing `<br />` tag after the question mark ?.
```
 <body>
    <p>Shall I compare thee to a summer's day?<br/> Thou art more lovely and more temperate</p>
  </body>
```








