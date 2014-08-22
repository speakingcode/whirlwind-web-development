# Web Applications

## What is web
- Client/Server
- HTTP
- Browser
- HTML/CSS/JavaScript

**REST** (Representational State Transfer) is an architectural approach that represents stateful resources in a stateless client-server environment.
- The worldwide web is a REST architecture
- RESTful web services are generally ones that map HTTP verbs (POST, GET, PUT, DELETE) to CRUD actions on corresponding resources

## Website vs Webapp

### Website

- mostly static
- publish/display content
- organized into structured documents, pages

#### Webpage

- html document
- text with HTML tags
- head, body
- elements
- CSS styling rules
- parsed into DOM tree (document object model)

#### Typical Website Flow

1. User clicks link/enter url
2. Browser sends GET request (url)
3. Web server finds resource
4. Web server sends response (HTML, text, image)
5. Browser parses/renders (HTML)

### Web Application

- functionality beyond displaying text/html or static content
- dynamic content and data/input-driven
- typically organized into forms, views, UI controls and dynamic workflows
- fit within context of a webpage/webpages
- "back-end" server-side functionality

#### Traditional Web Application Flow

1. User submits form or clicks link/button
2. Browser sends POST/PUT/GET request with form fields and other params
3. Web server passes request data to application
4. Application routes request to corresponding logic (url)
5. Logic executes, generates HTML page
6. Web server sends response (html)
7. Browser parses/renders HTML (reload)

#### Single Page Application (SPA) Flow

1. User action/etc triggers DOM event
2. JavaScript callback receives event
3. Browser makes *async* HTTP request to server w. data
4. Webserver passes data to application
5. Application routes request to corresponding logic
6. Logic executes, generates response payload (HTML snippet, XML, JSON...)
7. Webserver sends response
8. Browser receives response, executes JavaScript callback
9. Callback function reads response, updates models, manipulates/updates DOM in-place.

#### Advantages to SPA

- no page fetch/render
- smaller request payloads (no formatting/styling, no tags)
- asynchronous
- seamless, animated, responsive experience
- complex, event-driven applications
- treat front-end and back-end as separate, independent
- apply engineering principles on front-end

## Modern web development

### Front-End/Browser
#### HTML5/CSS3
- new tags, better semantics (header, nav, thead, video)
- canvas, svg
- advanced styling, positioning, animations
- well-defined browser behavior
- better system for updating/adopting standards

#### JavaScript
##### Richer APIs
- file I/O, persistent storage
- AJAX, XHR
- web worker
- browser history/location
- custom tags, data attributes

##### Proliferation of Libraries
- dom manipulation, ajax etc (jquery)
- mv* frameworks
- data-viz, svg (d3)
- graphics (webGL)
- persisted async communication (socketIO)

#### Evolution of Tools & Practices
- debuggers, dom explorer, consoles, profiling tools (Firebug/DevTools)
- OOP practices
- design patterns
- automated unit/integration testing, test tools
- build tools (compilation, minification)
- preprocessors (LESS/SASS, CoffeeScript, etc)
- packaging systems, repos
- dep management

### Back-End

#### Architecture

- RESTful API design
- Service-Oriented Architecture
- distributed architecture

#### Infrastructure

##### Virtualization

- infinite supply of cheap commodity servers
- no hardware pains
- aaS, pay-on-demand (cloud/VPS)
- scripted, automated provisioning, configuration and bootstrapping

##### DevOps

- infrastructure as code
- high scalability, etc. problems abstracted from application

##### Platform as a Service

- provide platform for application (containers, environments, etc)
- abstract infrastructure away
- google app engine, heroku

**Software as a Service**

## Application Stack

- webserver (apache, nginx)
- "gateway interface" (cgi, wsgi, rack, mod_php??)
- language platform (php, mri-ruby, rubinious, python, jvm, etc)
- container (gunicorn, phusion passenger)
- framework/application
- database(s)
- cache/key-value (memcached, redis)
- http cache (varnish)
- full-text search (elasticsearch, solr, lucene)

## Infrastructure

- load balancers/proxy (haproxy)
- application server(s)
- static content server/CDN
- database server(s)
- messaging, queues, workers (rabbitmq, celery)
- log server (logstash)


## Web Frameworks

### Full Stack/MVC

- rails, grails, play, laravel, zend, django...
- provide all/most components to build full-fledge web application in one place
- try to solve all of the common problems/tasks of web development
- opinionated about architecture, component structure, application design
- highly productive
-  maintainable, understandable
- usually include several tools
- many popular ones based on traditional, html-based request-response-reload
- not necessarily monolithic

#### Routers
- map requests & data to controller actions
 
#### Controllers
- read requests & determine action to call on models
- build and generate views from templates

#### Models
- represent domain-level concepts

#### Views
- representation of data in models (JSON, HTML, etc)

#### Templates
- file in format of view w. placeholders for code, variable references, etc. used to build actual views

#### Other
- database provisions
- asset management
- static file serving
- task runners, generators, etc
- environment configs
- test framework, test runners

### Micro Frameworks
- lightweight, RESTful-API based
- single/few file applications
- built around matching URL patterns and mapping to functions
- unopinionated, extensible, flexible (pick & choose)
- slim, sinatra, flask, express, spark, ratpack...

### Front-End frameworks
- all over the place thanks to javascript's super dynamic nature and bumpy history
- try to abstract some uglies of javascript, impose some sanity (object creation, factories, singletons...)
- often provide 'model' facility integrates w/ REST.
- range from lightweight/minimal (backbone) to full featured, opinionated (angular)

## Angular
- heroic, all-in-one, productive framework
- *declaritive* approach w. custom html tags/attributes
- correspond to *directives*, under-the-hood functionality which leverage templates to generate html
- automatic 2-way data binding between DOM and models
- factories for services (very similar to hibernate beans)
- dependency injection
- URL routing
- controllers
- "resources" (models w. REST integration)
