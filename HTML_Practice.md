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
The <head> element contains the metadata for a web page. Metadata is information about the page that isn't displayed directly on the web page. You'll see an example of this in the next exercise.
The opening and closing head tags (<head></head>) typically appear as the first item after your first HTML tag.
```
<!DOCTYPE html>
<html>
  <head></head>
</html>
```








