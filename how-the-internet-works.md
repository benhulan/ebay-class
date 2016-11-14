# Coding 101 for Product Managers

LESSON ONE:
## How the Internet Works
As simple as it sounds, this could really be the title for the entire course. Today, we need to cover the basic tools, system configuration and vocabulary necessary to build and maintain the modern web. 

Today we're going to learn some basic HTML and CSS, but before we do that, there are a couple of key concepts we need to introduce, to put all of this into context.

### The Request-Response Cycle
...in which we discuss Client-Server Architecture and the Request-Response Cycle.

**Obligatory Image of Client-Server Model:**

![Alt](http://kapsik.info/images/http.gif "basic client-server model")

#### Hypothesize:
- What is a web server?
- What is a client?

#### HyperText Transfer Protocol
**HTTP** is a protocol--a standardized system of communication--designed for two-way communication between computers. Any computer requesting information is a **client**. Any computer where the desired information is stored, is a **server**.

Those response `headers` include a very important piece of data called the **status code**. The status code tells us whether we have found what we are looking for. A code in the range of 100 - 199 will be informational.

**range** |  Meaning | Example situation(s)
100's | Information | Developers rarely do much with these response codes, as they happen before a request has been completed
200's | Success | Your request was successful! Record created/edited/deleted, document access granted
300's | Redirect | Client does not have permission to acces requested document, or it has been moved
400's | Client erorr | There's an error in the way the request was made, like requesting something that isn't there
500's | Server error | The request was consistent with protocol, but there's a problem with the response. Server down, data corrupted

[The Mozilla Developer Network (MDN)](https://developer.mozilla.org/en-US/) is my favorite source for general technical documentation of web standards. [Here is their straightforward reference to HTTP response status codes.](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) If you find all that stuff boring or just hard to remember, [here's a friendlier visual guide.](https://httpstatusdogs.com/)

#### What is a Browser, Really?
Your browser in no longer a tool for consuming content on the internet. A browser is a live **runtime**--a powerful computing environment--which lets us create and interact with media, data and documents. 

##### POP QUIZ 1: IS YOUR BROWSER THE CLIENT?
<summary>**What do you think?**
<details>
> Not exactly. Parts of your computer's operating system can be configured as a web client and that will certainly include a browser, if you have one. You can configure another part of your computer to be a web server, if you want.

**Proof:** Open your command line (`Terminal` in MacOS) and type:
```bash
$ curl http://www.google.com
```
<small>(Don't type the '$' -- that's an indicator for the command prompt.)</small>
</details></summary>


### The DOM


### HTML


### CSS


#### Exercise Link:

We're going to start with a simple, Personal Website.


[Table of Contents](./README.md#outline)