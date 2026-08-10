# Web Development Fundamentals

This repository contains notes and practical work covering the basic
concepts of web development, including frontend, backend, client-server
architecture, web servers, browsers, development tools, and basic web
architecture.

## Topics Covered

### 1. Frontend, Backend, and Full-Stack Development

-   **Frontend Development** --- The part of a website users see and
    interact with.
    -   Technologies: HTML, CSS, JavaScript, React, Angular
    -   Example: Product pages, buttons, menus, forms
-   **Backend Development** --- Server-side logic that processes
    requests and manages application data.
    -   Technologies: Node.js, Java, Python, PHP, C#
    -   Example: Authentication, order processing, APIs
-   **Full-Stack Development** --- Development involving both frontend
    and backend.
    -   Example: A complete e-commerce application

**In simple words:**

> Frontend = What the user sees\
> Backend = What happens behind the scenes\
> Full-stack = Frontend + Backend

------------------------------------------------------------------------

## 2. Client-Server Model

The client-server model allows a client, such as a web browser, to
request resources from a server.

``` text
             REQUEST
        "Give me example.com"
                 |
                 v
        +-----------------+
        |     CLIENT      |
        |   Web Browser   |
        +--------+--------+
                 |
                 | HTTP/HTTPS
                 v
        +-----------------+
        |   WEB SERVER    |
        | Apache/Nginx    |
        | Node.js etc.    |
        +--------+--------+
                 |
                 | RESPONSE
                 v
        +-----------------+
        |     CLIENT      |
        |   Web Browser   |
        +-----------------+
```

------------------------------------------------------------------------

## 3. How a Browser Displays a Web Page

The basic process is:

1.  The user enters a URL.
2.  The browser performs a DNS lookup to find the server's IP address.
3.  The browser establishes a connection with the server.
4.  The browser sends an HTTP/HTTPS request.
5.  The web server processes the request.
6.  The server returns resources such as HTML, CSS, JavaScript, images,
    and fonts.
7.  The browser parses the HTML and creates the DOM.
8.  CSS is processed to determine the page's appearance.
9.  JavaScript is executed when required.
10. The browser's rendering engine lays out and displays the webpage.

``` text
User enters URL
      |
      v
Browser
      |
      v
DNS Lookup
      |
      v
Web Server
      |
      v
HTTP Response
      |
      v
HTML + CSS + JavaScript
      |
      v
Browser Parsing & Rendering
      |
      v
Web Page Displayed
```

------------------------------------------------------------------------

## 4. Web Development Environment Tools

  -----------------------------------------------------------------------
  Tool                                Purpose
  ----------------------------------- -----------------------------------
  Visual Studio Code                  Code editor for HTML, CSS, and
                                      JavaScript

  Web Browser                         Runs and tests websites

  Git                                 Tracks changes in source code

  GitHub                              Hosts and manages Git repositories

  Node.js                             Runs JavaScript outside the browser
                                      and supports modern development
                                      tools

  npm                                 Installs and manages JavaScript
                                      packages

  Live Server                         Provides a local development server
                                      with automatic page refresh

  Terminal / Command Prompt           Executes development commands

  Browser Developer Tools             Helps inspect, debug, and test
                                      webpages
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 5. Web Server

A **web server** is software, and commonly the computer running that
software, that receives HTTP/HTTPS requests and returns web resources or
responses.

### Common Web Servers

-   Apache HTTP Server
-   Nginx
-   Microsoft IIS
-   LiteSpeed
-   Caddy

Example:

``` text
Browser
   |
   | HTTP Request
   v
Web Server
   |
   | HTTP Response
   v
Browser
```

------------------------------------------------------------------------

## 6. Roles in a Web Development Project

### Frontend Developer

Responsible for the user interface and client-side functionality.

Typical responsibilities:

-   HTML structure
-   CSS styling
-   JavaScript functionality
-   Responsive design
-   API integration
-   User experience

### Backend Developer

Responsible for server-side functionality and application logic.

Typical responsibilities:

-   APIs
-   Authentication
-   Business logic
-   Server-side processing
-   Database communication
-   Security

### Database Administrator (DBA)

Responsible for managing and maintaining databases.

Typical responsibilities:

-   Database creation and maintenance
-   Security and permissions
-   Backup and recovery
-   Performance monitoring
-   Query optimization
-   Data integrity

------------------------------------------------------------------------

## 7. VS Code Setup for HTML, CSS, and JavaScript

### Installation

Download Visual Studio Code from:

https://code.visualstudio.com/

Create a project folder such as:

``` text
WebDevelopment/
├── index.html
├── style.css
└── script.js
```

### Example `index.html`

``` html
<!DOCTYPE html>
<html>
<head>
    <title>My Web Page</title>
</head>
<body>
    <h1>Hello World</h1>
</body>
</html>
```

### Example `style.css`

``` css
body {
    background-color: lightblue;
}

h1 {
    color: navy;
}
```

### Example `script.js`

``` javascript
console.log("Hello from JavaScript!");
```

### Recommended VS Code Extensions

-   Live Server
-   Prettier - Code formatter
-   ESLint

> **Practical requirement:** Take a screenshot of the configured VS Code
> environment and add it to the project/assignment as evidence of the
> setup.

------------------------------------------------------------------------

## 8. Static vs Dynamic Websites

### Static Website

A static website generally serves fixed files and displays mostly the
same content to visitors.

**Characteristics:**

-   Fixed content
-   Simple to develop
-   Fast to serve
-   Usually does not require a database for basic content

**Example:** A simple college information website containing Home,
About, Courses, and Contact pages.

### Dynamic Website

A dynamic website generates or changes content based on users, data,
actions, authentication, or other conditions.

**Characteristics:**

-   Content can change
-   Usually uses backend programming
-   Often communicates with a database
-   Supports personalized content

**Example:** Amazon, where users can have different shopping carts,
orders, recommendations, and account information.

``` text
STATIC

Browser -> Web Server -> HTML/CSS/JS
                         |
                    Fixed Content


DYNAMIC

Browser -> Web Server -> Backend -> Database
                         |
                  Generated Response
```

------------------------------------------------------------------------

## 9. Five Web Browsers and Their Rendering Engines

A rendering engine interprets web technologies such as HTML and CSS and
converts them into the visual webpage displayed by the browser.

  Browser           Rendering Engine
  ----------------- ------------------
  Google Chrome     Blink
  Microsoft Edge    Blink
  Mozilla Firefox   Gecko
  Apple Safari      WebKit
  Opera             Blink

### Differences

Although browsers follow common web standards, their rendering engines
have different implementations. This can sometimes cause small
differences in how webpages are displayed or behave.

-   Chrome uses **Blink**.
-   Microsoft Edge uses **Blink**.
-   Opera uses **Blink**.
-   Firefox uses **Gecko**.
-   Safari uses **WebKit**.

------------------------------------------------------------------------

## 10. Basic Web Architecture

A typical modern web application consists of a client, APIs, a server,
and a database.

``` text
                    INTERNET
                       |
                       v
              +-----------------+
              |     CLIENT      |
              |     Browser     |
              |   HTML/CSS/JS   |
              +--------+--------+
                       |
                       | HTTP/HTTPS
                       v
              +-----------------+
              |      API        |
              |  REST / GraphQL |
              +--------+--------+
                       |
                       v
              +-----------------+
              |     SERVER      |
              | Backend Logic   |
              | Authentication  |
              | Business Logic  |
              +--------+--------+
                       |
                       | Database Query
                       v
              +-----------------+
              |    DATABASE     |
              | Users           |
              | Products        |
              | Orders          |
              +--------+--------+
                       |
                       | Data
                       v
              +-----------------+
              |     SERVER      |
              +--------+--------+
                       |
                       | API Response
                       v
              +-----------------+
              |     CLIENT      |
              |  Web Browser    |
              +-----------------+
```

### Real-World Example: Online Shopping

When a user clicks **Add to Cart**:

``` text
User
  |
  v
Browser
  |
  v
API Request
  |
  v
Backend Server
  |
  v
Database
  |
  v
Product Added to Cart
  |
  v
API Response
  |
  v
Browser Updates Cart
```

------------------------------------------------------------------------

## Quick Revision

``` text
FRONTEND
  -> User interface
  -> HTML + CSS + JavaScript

BACKEND
  -> Server-side logic
  -> APIs + Authentication + Business Logic

DATABASE
  -> Stores application data
  -> Users + Products + Orders

WEB SERVER
  -> Receives HTTP requests
  -> Sends HTTP responses

CLIENT
  -> Browser or application making requests

API
  -> Communication interface between application components

FULL STACK
  -> Frontend + Backend + Database interaction
```

## Conclusion

Web development is divided into several interconnected areas. Frontend
development focuses on what users see, backend development handles
server-side processing, and databases store application data. APIs
connect different parts of an application, while web servers deliver
resources and process requests. Understanding the client-server model
and basic web architecture provides a strong foundation for learning
modern web development.
