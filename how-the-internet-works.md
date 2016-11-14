# Coding 101 for Product Managers

LESSON ONE:
## How the Internet Works
As simple as it sounds, this could really be the title for the entire course. Today, we need to cover the basic tools, system configuration and vocabulary necessary to build and maintain the modern web. 

Today we're going to learn some basic HTML and CSS, but before we do that, there are a couple of key concepts we need to introduce, to put all of this into context.

### The Request-Response Cycle
...in which we discuss Client-Server Architecture and the Request-Response Cycle.

#### What is...?
- ...a web server?
- ...a client?
- ...the difference?

**Obligatory Image of Client-Server Model:**

![Alt](http://kapsik.info/images/http.gif "basic client-server model")

##### POP QUIZ 1: IS YOUR BROWSER THE CLIENT?
<summary>**What do you think?**
<details>
> Not exactly. Parts of your computer's operating system can be configured as a web client and that will certainly include a browser, if you have one. You can configure another part of your computer to be a web server, if you want.

**Proof:** Open your command line (`Terminal` in MacOS) and type:
```bash
$ curl http://www.google.com
```
<small>(Don't type the '$' -- that's an indicator for the command prompt.)</small>

#### So...What is a Browser, Really?
I would like to challenge you to stop thinking of your browser as a tool for consuming content on the internet. Replace that model with the knowledge that a browser is a live **runtime**--a powerful computing environment--which lets us create and interact with media, data and documents. More on browsers soon...

</details></summary>


#### HyperText Transfer Protocol
OK, great. So we have two or more computers that want to talk to each other. Next we need a set of standards for that communication so that all computers will understand what is being communicated without limiting the possibilities for the structure and content of that information.

**HTTP** is the protocol--the standardized system of communication--designed to enable two-way hypertext communication among computers. Any computer requesting information is the **client**. Any computer where the desired information is stored, is the **server**. This is the nervous system of the internet and is widely used for communication in closed networks, as well.

In the illustration above, the response headers include a very important data point called the **status code**. The status code tells us whether our server has found the document requested by a client. Here's a quick cheatsheet for server response codes:

**range** |  Meaning | Example situation(s)
100's | Information | Developers rarely do much with these response codes, as they happen before a request has been completed
200's | Success | Your request was successful! Record created/edited/deleted, document access granted
300's | Redirect | Client does not have permission to acces requested document, or it has been moved
400's | Client erorr | There's an error in the way the request was made, like requesting something that isn't there
500's | Server error | The request was consistent with protocol, but there's a problem with the response. Server down, data corrupted

[The Mozilla Developer Network (MDN)](https://developer.mozilla.org/en-US/) is my favorite source for general technical documentation of web standards. Here is [Mozilla's reference to HTTP response status codes.](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) 

If you find all that stuff boring or just hard to remember, [here's a friendlier visual guide.](https://httpstatusdogs.com/)

#### Further reflection:
- HTTP is just one protocol used in web development. Do you know of any others?

### The DOM
A lot of people struggle with the concept of **the DOM**. There's a lot to it, but the basics are pretty straightforward. The DOM is a representation of the architecture for your web document. Each webpage has its own DOM. The visual representation of the heirarchy of your content should be exactly the same as the written HTML.

![Alt](https://cloud.githubusercontent.com/assets/7320191/20251102/3ee9495e-a9cb-11e6-8955-ce2526c2ca82.png, "the DOM in visual and declarative form")

So documents in the DOM are made with two **declarative** languages:  HTML and CSS. The browser also knows how to interpret JavaScript, which is an **imperative** language (although JS can be written in a declarative, procedural/functional or object-oriented style).

There's one more thought I'd like to introduce regarding the DOM. In a couple of weeks we'll be diving into Node.js. Node has become the defacto library for server-side javascript. Whereas the root node of the DOM is the window, Node is not browser-based. Instead of a `window` object, Node begins with the `process`. Remember this:  it is important!

### HTML
Here is Mozilla's [Main Intro to HTML](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Introduction)
And, um, here is Mozilla's [Other Intro to HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML)

Please train yourself to avoid unsophisticated, outdated content such as [w3schools](http://www.w3schools.com/modern-web)

### CSS
Mozilla's [Intro to CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS)


## Exercise01
- Browse or read as much about HTML and CSS as you can. When you feel ready, dive into Exercise01: Personal Website Wireframe.
- In our next 1-3 classes we will add responsive CSS and interactive <forms> and <buttons> so try to focus on the basic architecture and content really make it perfect.


[Table of Contents](./README.md#outline)


## Responsive Layouts
Coming Soon

## Intro to Javascript
Coming Soon

## HTML Forms
Coming Soon
