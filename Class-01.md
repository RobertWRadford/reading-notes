# Introductory HTML and JavaScript

## Chapter 1 pg. 12-39

"HTML describes the structure of pages"
f.e.
```html
<html>
   <body>
     <h1> this is the main heading </h1>
     <p>This is a paragraph. It may be an introduction or some such thing.</p>
     <h2>This is a sub-heading and will be smaller in size</h2>
  </body>
</html>
```

The html and body brackets act like containers defining everything between them as their descriptor, much like { } encloses a function in programming.

You can add attributes to a tag line 
f.e. 
```html
<p lang="en-us"> english text </p>
```

A better structured page would include a 
```html
<head> 
  <title> this is the title </title>
</head>
```

## Chapter 8 pg. 176-199

to place a comment in HTML the syntax is as follows

```html
<!-- comment -->
```

One type of attribute you can give to a tag line is an ID to be able to designate it seperately from other similar data types.
Similarly a class attribute exists, which allows you to designate multiple tag lines as part of a group
the 'a' 'b' 'em' and 'img' tags are examples of inline elements and will continue on the same line as the preceeding tag
you can use the 'div' tag line to group things together in one block level box
You can use the 'span' tag to seperately identify a segment of text inside of a different tag, f.e.
```html
<p> this is some text. <span class="example"> I am typing it for an example</span>.</p>
```

the iframe tagline allows you to create a window to display a different page or widget in, for example a small google maps box on a webpage
it takes attributes of src (source, the url of the page to show) as well as height and width in pixels to use. Pre html5 the scrolling attribute as a binary yes/no enabled feature, frameborder is a 0 or 1 binary input for if a frame border should be placed around the web page, and in HTML5 seamless will strip away the scroll bars. 

The meta tagline goes inside the header, and while it is not visible text is important for describing the purpose of the site, keywords, author names, etc. for search engine results.

HTML has its own unique set of escape characters
[HTML5 escape characters]:(https://www.w3schools.com/html/html_entities.asp)

## Chapter 17 pg. 428-451

The 'header' and 'footer' taglines create a bar at the top and bottom of every page

The 'nav' tagline holds a navigational block such as a list of hyperlinks to other pages on the site

the 'article' tagline is used to seperate any component that could be a standalone piece such as an individual blog entry

the 'aside' tagline can be used to designate material related to the overall content of the page such as links to other pages on the site, or when used inside of an article it can be isolated relevance to that segment like a a glossary term

the 'section' tagline groups related groups together

The 'hgroup' tagline groups together multiple sub headings into one heading

To help older browsers properly interpret the intended structure you should include the following CSS to dictate what should be read as a block format
```CSS
header, section, footer, aside, nav, article, figure
{
display: block;}
```

