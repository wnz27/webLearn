# HTML

## What is HTML?

HTML is the language used to create the websites you visit everyday. It provides a logical way to structure content for websites.

Let's analyze the acronym "HTML," as it contains a lot of useful information. HTML stands for HyperText Markup Language.

A markup language is a computer language that defines the structure and presentation of raw text. 

Markup languages work by surrounding raw text with information the computer can interpret, "marking it up" to be processed.

In HTML, the computer can interpret raw text that is wrapped in HTML elements. 

These elements are often nested inside one another, with each containing information about the type and structure of the information to be displayed in the browser.

HyperText is text displayed on a computer or device that provides access to other text through links, 
also known as “hyperlinks.”

In fact, you probably clicked on many, many hyperlinks on your path to this Codecademy course!

Q:
In the code editor to the right, type your name in between `<h1> and </h1>`, then press Run.
`<h1>27</h1>`


## !DOCTYPE

Whether you realize it or not, when you read text, your brain must first identify the text's language. 

If you can understand that language, then your brain immediately begins to interpret the text. 

This same process happens whether you're reading a street sign, a book, or a name tag.

Web browsers work in a similar way. 
They must know what language a document is written in before they can process its contents.

You can let web browsers know that you are using HTML by starting your document with a document type declaration.

The declaration looks like this: <!DOCTYPE html>. This declaration is an instruction. 

It tells the browser what type of document to expect, along with what version of HTML is being used in the document.

<!DOCTYPE html> must be the first line of code in all of your HTML documents. 

If you don't use the declaration, your HTML code will likely still work, however, it's risky. 

For now, the browser will correctly assume that the html in <!DOCTYPE html> is referring to HTML5, as it is the current standard.

In the future, however, a new standard will override HTML5. 

Future browsers may assume you're using a different, newer standard, in which case your document will be interpreted incorrectly. 

To make sure your document is forever interpreted correctly, always include <!DOCTYPE html> at the very beginning of your HTML documents.
`<!DOCTYPE html>`


## Preparing for HTML

Great! Browsers that read your code will know to expect HTML when they attempt to read your file.

The <!DOCTYPE html> declaration is only the beginning, however. 

It indicates to the browser that you will use HTML in the document, but it doesn't actually add any HTML structure or content.
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


## HTML Structure

The rest of this lesson will focus on how HTML is structured and some tools developers use to make code easier to interpret.
HTML documents are organized as a collection of parent-child relationships. When an element is contained inside another element, it is considered the child of that element. The child element is said to be nested inside of the parent element.
```
<body>
  <p>Paragraph</p>
</body>
```
In the example above, the <p> element is nested inside the <body> element.
The <p> element is considered a child of the <body> element, the parent.
Since there can be multiple levels of nesting, this analogy can be extended to grandchildren, 
great-grandchildren and beyond. Let's consider a more complicated example:
```
<body>
  <div>
    <h1>Student</h1>
    <p>Get Started</p>
  </div>
</body>
```
In this example, the `<body>` element is the parent of the` <div> `element. 
Both the `<h1> and <p> `elements are children of the `<div> `element. 
Because the `<h1> and <p>` elements are in the same level, they are considered siblings,
and are both grandchildren of the <body> element.
Understanding this hierarchy is important, because child elements can inherit attributes from their parent element.
	
Q:
1. Add the paragraph below as a child of the div element.
`<p>This paragraph is a child of the div element</p>`
2. Add the paragraph below as a child of the body element.
`<p>This paragraph is a child of the body element</p>`
```
<!DOCTYPE html>
<html>
  <head>
    <title>Hello World</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <div>
			<p>This paragraph is a child of the div element</p>
    </div>
  <p>This paragraph is a child of the body element</p>
  </body>
</html>
```
display on web:
```
Hello World
This paragraph is a child of the div element
```

## Whitespace

As the code in an HTML file grows, it becomes increasingly difficult to keep track of how elements are related. Programmers use two tools to visualize the relationship between elements: whitespace and indentation.
Both tools take advantage of the fact that the position of elements in a browser is independent of the amount of whitespace or indentation in the index.html file.
For example, if you wanted to increase the space between two paragraphs on your web page, you would not be able to accomplish this by adding space between the paragraph elements in the index.html file. The browser ignores whitespace in HTML files when it renders a web page, so it can be used as a tool to make code easier to read and follow.
What makes the example below difficult to read?

```
<body><p>Paragraph 1</p><p>Paragraph 2</p></body>
```
You have to read the entire line to know what elements are present. Compare the example above to this:
```
<body>
<p>Paragraph 1</p>
<p>Paragraph 2</p>
</body>
```
This example is easier to read, because each element is on its own line. While the first example required you to read the entire line of code to identify the elements, this example makes it easy to identify the body tag and two paragraphs.
A browser renders both examples the same way:
```
Paragraph 1
Paragraph 2
```
In the next exercise you will learn how to use indentation to help visualize nested elements.
Q：
Use whitespace to make the code more readable by putting each element on its own line.
```
<!DOCTYPE html>
<html>
  <body>
    <h1>Whitespace</h1>
    <p>Whitespace and indentation make html documents easier to read.       </p>
  </body>
</html>
```

## Indentation

The second tool web developers use to make the structure of code easier to read is indentation.
The [World Wide Web Consortium](https://www.w3.org/Consortium/), or W3C, is responsible for maintaining the style standards of HTML. At the time of writing, the W3C recommends 2 spaces of indentation when writing HTML code. Although your code will work without exactly two spaces, this standard is followed by the majority of professional web developers. Indentation is used to easily visualize which elements are nested within other elements.
```
<body>
  <p>Paragraph 1</p>
  <div>
    <p>Paragraph 2</p>
  </div>
</body>
```
In the example above, Paragraph 1 and the <div> tag are nested inside of the <body> tag, so they are indented two spaces. The Paragraph 2 element is nested inside of the <div> tag, so it is indented an additional two spaces.
The spaces are inserted using the spacebar on your keyboard.
Q:
Indent the code in index.html to match the W3C standards.
```
<body>
  <h1>Whitespace</h1>    
  <div>
    <p>Whitespace and indentation make html documents easier to read.</p>
  </div>  
</body>
```

## Comments

HTML files also allow you to add comments to your code.
Comments begin with `<!--` and end with `-->`. Any characters in between will be ignored by your browser.
`<!-- This is a comment that the browser will not display. -->`
Including comments in your code is helpful for many reasons:
They help you (and others) understand your code if you decide to come back and review it at a much later date.
They allow you to experiment with new code, without having to delete old code.
```
<!-- Favorite Films Section -->
<p>The following is a list of my favorite films:</p>
```
In this example, the comment is used to denote that the following text makes up a particular section of the page.
`<!-- <p> Test Code </p> -->`
In the example above, a valid HTML element (a paragraph element) has been "commented out." This practice is useful when there is code you want to experiment with, or return to, in the future.


## Review
Congratulations on completing the first lesson of HTML & CSS! You are well on your way to becoming a skilled web developer.
Let's review what you've learned so far:
1. HTML stands for HyperText Markup Language and is used to create the structure and content of a webpage.
2. Most HTML elements contain opening and closing tags with raw text or other HTML tags between them.
3. Single-closing tags cannot enclose raw text or other elements.
4. Comments are written in HTML using the following syntax: <!-- comment -->.
5. HTML elements can be nested inside other elements. The enclosed element is the child of the enclosing parent element.
6. Whitespace between HTML elements helps make code easier to read while not changing how elements appear in the browser.
7. Indentation also helps make code easier to read. It makes parent-child relationships visible.
8. The <!DOCTYPE html> declaration should always be the first line of code in your HTML files.
9. The <html> element will contain all of your HTML code.
10. Information about the web page, like the title, belongs within the <head> of the page.
11. You can add a title to your web page by using the <title> element, inside of the head.
12. A webpage's title appears in a browser's tab.
13. Code for visible HTML content is placed inside of the <body> element.
What you learned in this lesson constitutes the required setup for all HTML files. The rest of the course will teach you more about how to add content using HTML.
Q:
1.
Add a body to the web page.
2.
Copy and paste the following line of code within the body of the index.html file:
`<h1>Hello World!</h1>`
```
<!DOCTYPE html>
<html>
  <head>
  	<title>My Coding Journey</title>
  </head>
  <body>
    <h1>Hello World!</h1>
  </body>
</html>
```

# Fashion Blog
In this course, you will make a fashion blog using HTML. The blog will describe a designer's experience at New York Fashion Week. The blog will contain images, links, lists, and more HTML elements. You can see the completed project [here](https://s3.amazonaws.com/codecademy-content/courses/learn-html/elements-and-structure/fashion.html)!

1. Add the basic code for a website to be structured properly (also called boilerplate code).

2. Title your website `Everyday with Isa`

3. Directly below the opening <body> tag, add an `<h1>` that says:
`An Insider's Guide to NYFW`
Below that, add an `<h2>` that says:
`Getting Tickets & Picking the Shows`
Below that, add an `<h2>` that says:
`Dressing for the Shows`
	
4. Between the `<h1>` and first `<h2>` tag, add a `<p>` tag that says:
NYFW can be both amazingly fun & incredibly overwhelming, 
especially if you've never been. Luckily, 
I'm here to give you an insider's guide and make your first show a pleasurable experience. 
By taking my tips and tricks, and following your gut, you'll have an unforgettable experience!
	
5. Between the first and second `<h2>` tags, add a `<p>` tag that says:
If you're lucky or connected you can get an invite, sans the price tag.
But I wasn't so lucky or connected my first 2 years so I'm here to help you out. 
First, plan out which shows are most important to you and make a schedule and this is a biggie:SET A BUDGET. 
If you're worrying about blowing your cash the whole time you won't have fun.
Then check out prices, days, and times and prioritize the designers you want to see most. 
Lastly, purchase your tickets and get excited!
	
	
6. After the last `<h2>` tag, add a `<p>` tag that says:
Always be true to your own sense of style, if you don't you'll be uncomfortable the whole time and it will show. 
Remember, NYFW is about expressing yourself and taking in what the designers have chosen to express through their new lines.
Also it's important to wear shoes you'll be comfortable in all day. Obviously you want to look good,
but you'll be on your feet all day long, so be prepared.
	
	
7. Let's add some pictures to our blog post. Above each paragraph, add an <img> tag and set its src to be one of the following links
```
https://s3.amazonaws.com/codecademy-content/courses/learn-html/elements-and-structure/image-one.jpeg
https://s3.amazonaws.com/codecademy-content/courses/learn-html/elements-and-structure/image-two.jpeg
https://s3.amazonaws.com/codecademy-content/courses/learn-html/elements-and-structure/image-three.jpeg
```
8. 
Your first blog post is complete! Now let’s add the author. Below the opening body tag, add an `<img>` tag with
```
src="https://s3.amazonaws.com/codecademy-content/courses/learn-html/elements-and-structure/profile.jpg".
```
9. Below the `<img>` tag, add an `<h3>` that says `by Isabelle Rodriguez | 1 day ago`
10. Let’s make a list of some related blog posts. Beneath the last paragraph, add a `<h4>` tag that says `Related Content`. Underneath that, create an unordered list.

11. The unordered list should have 4 <li>s. They should be:
* How To Style Boyfriend Jeans
* When Print Is Too Much
* The Overalls Trend
* Fall's It Color: Blush
12. Add a link for more information about New York Fashion Week. In your first paragraph, the first word is NYFW. Surround that word with <a> tags. In the tag, set:        
```
href="https://en.wikipedia.org/wiki/New_York_Fashion_Week" and target="_blank"
```
13.  
At the bottom of your body, add a new <div> and set its id='contact'. Inside the div, create a new <p> tag and put the following contact information inside of it.
```
email: isa@fashionblog.com | phone: 917-555-1098 | address: 371 284th St, New York, NY, 10001
```
14. Inside the contact div, Put `<strong>` opening and closing tags around email, phone, and address
	
15. Let’s make the profile picture a link to the contact section of your webpage. Find your profile `<img>` tag, and surround it by opening and closing <a> tags. In the <a> tag, set `href='#contact'`.

```
<!DOCTYPE html>
<html>
  <head>
    <title>Everyday with Isa</title>
  </head>
  <body>

    <a href="#contact">
        <img src="https://s3.amazonaws.com/codecademy-content/courses/learn-html/elements-and-structure/profile.jpg">
    </a>  
    
    <h3>by Isabelle Rodriguez | 1 day ago</h3>
    <h1>An Insider's Guide to NYFW</h1>

    <img src="https://s3.amazonaws.com/codecademy-content/courses/learn-html/elements-and-structure/image-one.jpeg">
    <p> <a href="https://en.wikipedia.org/wiki/New_York_Fashion_Week" target="_blank">NYFW</a> can be both amazingly fun & incredibly overwhelming, especially if you've never been. 
    Luckily, I'm here to give you an insider's guide and make your first show a pleasurable experience. 
    By taking my tips and tricks, and following your gut, you'll have an unforgettable experience!</p>

    <h2>Getting Tickets & Picking the Shows</h2>

    <img src="https://s3.amazonaws.com/codecademy-content/courses/learn-html/elements-and-structure/image-two.jpeg">
    <p>If you're lucky or connected you can get an invite, sans the price tag. 
    But I wasn't so lucky or connected my first 2 years so I'm here to help you out. 
    First, plan out which shows are most important to you and make a schedule and this is a biggie: SET A BUDGET. 
    If you're worrying about blowing your cash the whole time you won't have fun. 
    Then check out prices, days, and times and prioritize the designers you want to see most. 
    Lastly, purchase your tickets and get excited!</p>

    <h2>Dressing for the Shows</h2>

    <img src="https://s3.amazonaws.com/codecademy-content/courses/learn-html/elements-and-structure/image-three.jpeg">
    <p>Always be true to your own sense of style, if you don't you'll be uncomfortable the whole time and it will show. 
    Remember, NYFW is about expressing yourself and taking in what the designers have chosen to express through their new lines. 
    Also it's important to wear shoes you'll be comfortable in all day. 
    Obviously you want to look good, but you'll be on your feet all day long, so be prepared.</p>

    <h4>Related Content</h4>
    <li> How To Style Boyfriend Jeans</li>
    <li>When Print Is Too Much</li>
    <li>The Overalls Trend</li>
    <li>Fall's It Color: Blush</li>

  </body>

  <div id="contact">
      <p>
          <strong>email</strong>: isa@fashionblog.com |
          <strong>phone</strong>: 917-555-1098 |
          <strong>address</strong>: 371 284th St, New York, NY, 10001
      </p>
  </div>
</html>
```

# HTML Tables
## Why Tables?
There are many websites on the Internet that display information like stock prices, sports scores, invoice data, and more. This data is naturally tabular in nature, meaning that a table is often the best way of presenting the data.
In this part of the course, you'll learn how to use HTML to present tabular data to users.
```
<!DOCTYPE html>
<html>
<head>
  <title>Ship To It - Company Packing List</title>
  <link href="https://fonts.googleapis.com/css?family=Lato: 100,300,400,700|Luckiest+Guy|Oxygen:300,400" rel="stylesheet">
  <link href="style.css" type="text/css" rel="stylesheet">
</head>
<body>

  <ul class="navigation">
    <li><img src="https://s3.amazonaws.com/codecademy-content/courses/web-101/unit-9/htmlcss1-img_logo-shiptoit.png" height="20px;"></li>
    <li class="active">Action List</li>
    <li>Profiles</li>
    <li>Settings</li>
  </ul>

  <div class="search">Search the table</div>

  <table>
    <thead>
      <tr>
        <th>Company Name</th>
        <th>Number of Items to Ship</th>
        <th>Next Action</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th>Adam's Greenworks</th>
        <td>14</td>
        <td>Package Items</td>
      </tr>
      <tr>
        <th>Davie's Burgers</th>
        <td>2</td>
        <td>Send Invoice</td>
      </tr>
      <tr>
        <th>Baker's Bike Shop</th>
        <td>3</td>
        <td>Send Invoice</td>
      </tr>
      <tr>
        <th>Miss Sally's Southern</th>
        <td>4</td>
        <td>Ship</td>
      </tr>
      <tr>
        <th>Summit Resort Rentals</th>
        <td>4</td>
        <td>Ship</td>
      </tr>
      <tr>
        <th>Strike Fitness</th>
        <td>1</td>
        <td>Enter Order</td>
      </tr>
      </tbody>
  </table>

</body>
</html>
```

## Table Rows
In many programs that use tables, the table is already predefined for you, meaning that it contains the rows, columns, and cells that will hold data. In HTML, all of these components must be created.
The first step in entering data into the table is to add rows using the table row element: `<tr>`.
```
<table>
  <tr>
  </tr>
  <tr>
  </tr>
</table>
```
In the example above, two rows have been added to the table.
## Table Data
Rows aren't sufficient to add data to a table. Each cell element must also be defined. In HTML, you can add data using the table data element: <td>.
```
<table>
  <tr>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
```
In the example above, two data points (73 and 81) were entered in the one row that exists. By adding two data points, we created two cells of data.
If the table were displayed in the browser, it would show a table with one row and two columns.
Q:
In the second row, add three cells of data. The cells should contain the following data, in order:
```
Adam's Greenworks
14
Package Items
```
```
<table>
    <tr>
      <td>Adam's Greenworks</td>
      <td>14</td>
      <td>Package Items</td>
    </tr>
    <tr></tr>
  </table>
```

## Table Headings
Table data doesn't make much sense without titles to describe what the data represents.
To add titles to rows and columns, you can use the table heading element:` <th>`.
The table heading element is used just like a table data element, except with a relevant title. Just like table data, a table heading must be placed within a table row.
```
<table>
  <tr>
    <th></th>
    <th scope="col">Saturday</th>
    <th scope="col">Sunday</th>
  </tr>
  <tr>
    <th scope="row">Temperature</th>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
```
What happened in the code above?
First, a new row was added to hold the three headings: a blank heading, a `Saturday` heading, and a `Sunday` heading. The blank heading creates the extra table cell necessary to align the table headings correctly over the data they correspond to.
In the second row, one table heading was added as a row title: `Temperature`.
Note, also, the use of the `scope` attribute, which can take one of two values:
`row` - this value makes it clear that the heading is for a row.
`col` - this value makes it clear that the heading is for a column.
HTML code for tables may look a little strange at first, but analyzing it piece by piece helps make the code more understandable.
Q:
In the first row, add three table headings. The headings should contain the following data, in order:
Company Name
Number of Items to Ship
Next Action
These headings will add meaning to the rest of the data in the table.
```
<html>
    <table>
        <tr>
            <th scope="col">Company Name</th>
            <th scope="col">Number of Items to Ship</th>
            <th scope="col">Next Action</th>
        </tr>
        <tr>
            <td>Adam's Greenworks</td>
            <td>14</td>
            <td>Package Items</td>
        </tr>
    </table>
</html>
```

## Table Borders
So far, the tables you've created have been a little difficult to read because they have no borders.
In older versions of HTML, a border could be added to a table using the border attribute and setting it equal to an integer. This integer would represent the thickness of the border.
```
<table border="1">
  <tr>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
```
The code in the example above is following is deprecated, so please don't use it. It's meant to illustrate older conventions you may come across when reading other developers' code.
The browser will likely still interpret your code correct if you use the border attribute, but that doesn't mean the attribute should be used. Instead, you can achieve the same effect using CSS.
```
table, td {
  border: 1px solid black;
}
```
The code in the example above uses CSS instead of HTML to show table borders.
We're going to need some more data in the table. Add the following data to the table. Make sure to place it after the second table row.
```
<tr>
  <td>Davie's Burgers</td>
  <td>2</td>
  <td>Send Invoice</td>
</tr>
<tr>
  <td>Baker's Bike Shop</td>
  <td>3</td>
  <td>Send Invoice</td>
</tr>
<tr>
  <td>Miss Sally's Southern</td>
  <td>4</td>
  <td>Ship</td>
</tr>
<tr>
  <td>Summit Resort Rentals</td>
  <td>4</td>
  <td>Ship</td>
</tr>
<tr>
  <td>Strike Fitness</td>
  <td>1</td>
  <td>Enter Order</td>
</tr>
```
Style.css:
```
body {
    background: #EEE;
    margin: 0;
    padding: 0;
  }
  
  /* Navigation */
  
  .navigation {
    box-sizing: border-box;
    background-color: paleturquoise;
    overflow: auto;
    padding: 18px 50px;
    position: relative;
    top: 0;
    width: 100%;
    z-index: 999;
  }
  
  ul {
    padding: 0;
    margin: 0;
  }
  
  li {
    color: black;
    display: inline-block;
    font-family: 'Oxygen', sans-serif;
    font-size: 16px;
    font-weight: 300;
    letter-spacing: 2px;
    margin: 0;
    padding: 20px 18px 10px 18px;
    text-transform: uppercase;
  }
  
  .active {
    color: hotpink;
  }
  
  /* Table */
  
  table {
    height: 40%;
    left: 10%;
    margin: 20px auto;
    overflow-y: scroll;
    position: static;
    width: 80%;
  }
  
  thead th {
    background: #88CCF1;
    color: #FFF;
    font-family: 'Lato', sans-serif;
    font-size: 16px;
    font-weight: 100;
    letter-spacing: 2px;
    text-transform: up;
  }
  
  tr {
    background: #f4f7f8;
    border-bottom: 1px solid #FFF;
    margin-bottom: 5px;
  }
  
  th, td {
    font-family: 'Lato', sans-serif;
    font-weight: 400;
    padding: 20px;
    text-align: left;
    width: 33.3333%;
    border: 1px solid black;
  }
  
  .search {
    background-color: #FFF;
    border: 1px solid #DDD;
    border-radius: 3px;
    color: #AAA;
    padding: 20px;
    margin: 50px auto 0px auto;
    width: 77%;
  }
```

## Spanning Columns
What if the table contains data that spans multiple columns?
For example, a personal calendar could have events that span across multiple hours, or even multiple days.
Data can span columns using the `colspan` attribute. The attributes accepts an integer (greater than or equal to 1) to denote the number of columns it spans across.
```
<table>
  <tr>
    <th>Monday</th>
    <th>Tuesday</th>
    <th>Wednesday</th>
  </tr>
  <tr>
    <td colspan="2">Out of Town</td>
    <td>Back in Town</td>
  </tr>
</table>
```
In the example above, the data Out of Town spans the Monday and Tuesday table headings using the value 2 (two columns). The data Back in Town appear only under the Wednesday heading.



## Spanning Rows
Data can also span multiple rows using the `rowspan` attribute.
The `rowspan` attribute is used for data that spans multiple rows (perhaps an event goes on for multiple hours on a certain day). It accepts an integer (greater than or equal to 1) to denote the number of rows it spans across.
```
<table>
  <tr> <!-- Row 1 -->
    <th></th>
    <th>Saturday</th>
    <th>Sunday</th>
  </tr>
  <tr> <!-- Row 2 -->
    <th>Morning</th>
    <td rowspan="2">Work</td>
    <td rowspan="3">Relax</td>
  </tr>
  <tr> <!-- Row 3 -->
    <th>Afternoon</th>
  </tr>
  <tr> <!-- Row 4 -->
    <th>Evening</th>
    <td>Dinner</td>
  </tr>
</table>
```
In the example above, there are four rows:
1. The first row contains an empty cell and the two column headings.
2. The second row contains the Morning row heading, along with Work, which spans two rows under the Saturday column. The "Relax" entry spans three rows under the Sunday column.
3. The third row only contains the Afternoon row heading.
4. The fourth row only contains the Dinner entry, since "Relax" spans into the cell next to it.
If you'd like to see how the browser interprets the code above, feel free to copy and paste it into the code editor to understand it a little better.


## Table Body
Over time, a table can grow to contain a lot of data and become very long. When this happens, the table can be sectioned off so that it is easier to manage.
Long tables can be sectioned off using the table body element: `<tbody>`.
The `<tbody>` element should contain the all of the table's data, excluding the table headings (more on this in a later exercise).
```
<table>
  <tbody>
    <tr>
      <th></th>
      <th>Saturday</th>
      <th>Sunday</th>
    </tr>
    <tr>
      <th>Morning</th>
      <td rowspan="2">Work</td>
      <td rowspan="3">Relax</td>
    </tr>
    <tr>
     <th>Afternoon</th>
    </tr>
    <tr>
      <th>Evening</th>
      <td>Dinner</td>
    </tr>
  </tbody>
</table>
```
In the example above, all of the table data is contained within a table body element. Note, however, that the headings were also kept in the table's body — we'll change this in the next exercise.
Q:
Enclose rows 2, 3, 4, 5, and 6 of the table in a `<tbody>` element.

## Table Head
In the last exercise, the table's headings were kept inside of the table's body. When a table's body is sectioned off, however, it also makes sense to section off the table's headings using the `<thead>` element.
```
<table>
  <thead>
    <tr>
      <th></th>
      <th>Saturday</th>
      <th>Sunday</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Morning</th>
      <td rowspan="2">Work</td>
      <td rowspan="3">Relax</td>
    </tr>
    <tr>
     <th>Afternoon</th>
    </tr>
    <tr>
      <th>Evening</th>
      <td>Dinner</td>
    </tr>
  </tbody>
</table>
```
In the example above, the only new element is `<thead>`. The table headings are contained inside of this element. Note that the table's head still requires a row in order to contain the table headings.
Enclose the first row of the table in a `<thead>` element.


## Table Footer
The bottom part of a long table can also be sectioned off using the <tfoot> element.
```
<table>
  <thead>
    <tr>
      <th>Quarter</th>
      <th>Revenue</th>
      <th>Costs</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Q1</th>
      <td>$10M</td>
      <td>$7.5M</td>
    </tr>
    <tr>
      <th>Q2</th>
      <td>$12M</td>
      <td>$5M</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>Total</th>
      <td>$22M</td>
      <td>$12.5M</td>
    </tr>
  </tfoot>
</table>
```
In the example above, the footer contains the totals of the data in the table. Footers are often used to contain sums, differences, and other data results.
Add a table footer at the bottom of the table using the <tfoot> element. Inside of the footer, add the following data:
```
<td>Total</td>
<td>28</td>
```

## Styling with CSS
Tables, by default, are very bland. They have no borders, the font color is black, and the typeface is the same type used for other HTML elements.
You can use CSS to style tables just like you have done in the past. Specifically, you can change style the various aspects mentioned above.
```
table, th, td {
  border: 1px solid black;
  font-family: Arial, sans-serif;
  text-align: center;
}
```
The code in the example above demonstrates just some of the various table aspects you can style using the CSS properties you learned about earlier.
In style.css, change the font size of all table headings and table data to 18 pixels.

## HTML Tables
Great job! In this lesson, you learned how to create a table, add data to it, and section the table into smaller parts that make it easier to read.
Let's review what you've learned so far:
1. The <table> element creates a table.
2. The `<tr>` element adds rows to a table.
3. To add data to a row, you can use the <td> element.
4. Table headings clarify the meaning of data. Headings are added with the` <th>` element.
5. Table data can span columns using the `colspan` attribute.
6. Table data can span rows using the `rowspan` attribute.
7. Tables can be split into three main sections: a head, a body, and a footer.
8. A table's head is created with the `<thead>` element.
9. A table's body is created with the `<tbody>` element.
10. A table's footer is created with the `<tfoot>` element.
11. All the CSS properties you learned about in this course can be applied to tables and their data.
Congratulations on completing HTML Tables!
```
<!DOCTYPE html>
<head>
        <title>Ship To It - Company Packing List</title>
        <link href="https://fonts.googleapis.com/css?family=Lato: 100,300,400,700|Luckiest+Guy|Oxygen:300,400" rel="stylesheet">
        <link href="style.css" type="text/css" rel="stylesheet">
      </head>
      <body>
      
        <ul class="navigation">
          <li><img src="https://s3.amazonaws.com/codecademy-content/courses/web-101/unit-9/htmlcss1-img_logo-shiptoit.png" height="20px;"></li>
          <li class="active">Action List</li>
          <li>Profiles</li>
          <li>Settings</li>
        </ul>
      
        <div class="search">Search the table</div>
        
        <table>
          <thead>
          <tr>
            <th>Company Name</th>
            <th>Number of Items to Ship</th>
            <th>Next Action</th>
          </tr>
          </thead>
          <tbody>
          <tr>
            <td>Adam's Greenworks</td>
            <td>14</td>
            <td>Package Items</td>
          </tr>
          <tr>
        <td>Davie's Burgers</td>
        <td>2</td>
        <td>Send Invoice</td>
      </tr>
      <tr>
        <td>Baker's Bike Shop</td>
        <td>3</td>
        <td>Send Invoice</td>
      </tr>
      <tr>
        <td>Miss Sally's Southern</td>
        <td rowspan="2">4</td>
        <td>Ship</td>
      </tr>
      <tr>
        <td>Summit Resort Rentals</td>
        <td>Ship</td>
      </tr>
    </tbody>
      <tr>
        <td colspan="2">Strike Fitness</td>
        <td>Enter Order</td>
      </tr>
      <tr>
            <th>Monday</th>
            <th>Tuesday</th>
            <th>Wednesday</th>
          </tr>
          <tr>
            <td colspan="2">Out of Town</td>
            <td>Back in Town</td>
          </tr>
          <tr> <!-- Row 1 -->
            <th></th>
            <th>Saturday</th>
            <th>Sunday</th>
          </tr>
          <tr> <!-- Row 2 -->
            <th>Morning</th>
            <td rowspan="2">Work</td>
            <td rowspan="3">Relax</td>
          </tr>
          <tr> <!-- Row 3 -->
            <th>Afternoon</th>
          </tr>
          <tr> <!-- Row 4 -->
            <th>Evening</th>
            <td>Dinner</td>
          </tr>
          <tfoot>
              <tr>
                    <td>Total</td>
                    <td>28</td>
              </tr>
          </tfoot>
        </table>
      </body>

```
Style.css:
```
body {
    background: #EEE;
    margin: 0;
    padding: 0;
  }
  
  /* Navigation */
  
  .navigation {
    box-sizing: border-box;
    background-color:#88CCF1;
    overflow: auto;
    padding: 18px 50px;
    position: relative;
    top: 0;
    width: 100%;
    z-index: 999;
  }
  
  ul {
    padding: 0;
    margin: 0;
  }
  
  li {
    color: black;
    display: inline-block;
    font-family: 'Oxygen', sans-serif;
    font-size: 16px;
    font-weight: 300;
    letter-spacing: 2px;
    margin: 0;
    padding: 20px 18px 10px 18px;
    text-transform: uppercase;
  }
  
  .active {
    color: hotpink;
  }
  
  /* Table */
  
  table {
    height: 40%;
    left: 10%;
    margin: 20px auto;
    overflow-y: scroll;
    position: static;
    width: 80%;
    font-size: 18px;
  }
  
  thead th {
    background: plum;
    color: #FFF;
    font-family: 'Lato', sans-serif;
    font-size: 16px;
    font-weight: 100;
    letter-spacing: 2px;
    text-transform: up;
  }
  
  tr {
    background: #f4f7f8;
    border-bottom: 1px solid #FFF;
    margin-bottom: 5px;
  }
  
  th, td {
    font-family: 'Lato', sans-serif;
    font-weight: 400;
    padding: 20px;
    text-align: left;
    width: 33.3333%;
    border: 1px solid black;
  }
  
  .search {
    background-color: #FFF;
    border: 1px solid #DDD;
    border-radius: 3px;
    color: #AAA;
    padding: 20px;
    margin: 50px auto 0px auto;
    width: 77%;
  }
```


