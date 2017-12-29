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









