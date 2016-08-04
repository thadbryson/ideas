# App Patterns

I'm constantly repeating myself in software. Which defeats a main purpose of software. There are a lot of things
that are used over and over again.

I want a nice checklist to use for when you're starting a new project of choices that need to be made. This can be
used when deciding on a framework, building your own framework, or building a new app.

## Things to think about
1. Semantics - There should be a system to how you name things.
2. DRY - "DON'T REPEAT YOURSELF" Make sure you don't see copy and pasted code.

## Specifications of your App
* What are the user needs of this app?
* How many people do we expect to use this right away? Not a fairy tail dream about 1 billion users in 6 months.
* Audience?
 - Ages? Is this for elderly people? The young?
 - Screen resolutions?
 - Browsers? What version of IE do you need to support? IE11+ maybe? Or do you need to support IE7?
 - Where do these people live?
  - What languages do you need to support? I mean like English, Spanish, Swahili?
  - Are you going to need language switching?
  - Currency conversion?
   - How are you going to get updates for that? They change daily.
* Platform?
 - On a mobile app?
  - Do you need responsive design?
  - Native application with iOS and Android?
  - Are you handling touch?
 - Desktop?
  - What screen resolutions?
* Responses?
 - HTML and JSON?
 - Errors?
* Responsive design?
* API
 - RESTful API
 - What methods are supported and how?
  - GET
  - POST
  - PUT/PATCH
  - DELETE
 - Tokens for User authentication?

## Code - server
* Architecure?
 - MVC (model-view-controller) or something else?
 - Flat files all over the place?
* Model system?
 - What fields are on every model? "createdAt", "updatedAt"?
 - How do you insert and update models?
 - How do your models interact with forms on your system?
 - Use an ORM? Doctrine, Eloquent, Propel, or none?
 - Database abstraction layer?
  - Does it adequately prevent SQL injection attacks?
  - Can it handle database types you need? MySQL, Oracle, Postgres, etc?
 - CRUD actions?
  - save()? Insert or update.
  - delete()? Delete the model?
  - How do you handle retrieving the data?
* Controllers?
* View system?
 - A template system?
 - What features does the template system have?
  - Extend templates?
  - Include templates?
  - Helpers for outputting links, forms, etc?
* Routing. How do you go from an HTTP GET with URL "/user/1/json" to a JSON response?
 - What HTTP methods do what?
 - Are you going to use RESTful design?
 - How does your system know which controller::action to call?
 - Naming conventions for these things?
 - How do you handle the configurations?
 - Do you have standardized parameter names?
* Loading and autoloading of files? Use Composer?
* Messaging to users
 - E-mails?
 - Text messages?
 - Flash messages to the screen after actions?
* Validation
 - For your data models?
* Configuration?
 - What format? Vanilla PHP, YAML, INI, XML, JSON, or something else?
 - What will be configurable?
* Events and queues
 - What things can be ran outside your controller actions?
 - Should some events be triggered after an action? Example: When a customer orders a t-shirt on your site should
 the confirmation email be sent later? Like 1 minute later? If there's a failure with the e-mail system your orders
 won't be interrupted.
* CLI Command line interface
 - What things can you execute on the command line?
 - What commands should be cronned?
* Reporting
 - Table view of data?
  - Headers?
  - What should be sortable?
  - Can we edit data inline?
 - What filters should we use?
 - Exports to CSV, Excel, or PDF?
 - Save the reports?
 - E-mail the reports?
 - Print the reports directly?
* Pagination
 - Page numbers. Default 1?
 - Size? What options? 10, 20, and 100?
 - Sorting?
 - UI component? How are you going to display all this to the user?
 - Can the User view the same thing when they come back to this page?
* Dependency Injection
 - Configuration for this?
 - How do you prevent circular references? Make sure when creating objects one object doesn't use another object that
 uses itself. Creates a fatal error. You get an infinite loop with them creating each other.
 - Access this? One global variable, global function, or embedded into your system?
* Forms
 - Interact with form data?
 - Pull from POST and GET? Other methods like DELETE and PATCH?
 - CSRF protection?
 - Build forms on the frontend?
* Requests? HTTP Requests.
 - CSRF protection?
 - Get POST and GET data.
 - Sanitize data for security problems?
  - Remove HTML to prevent XSS attacks?
  - Limit number of email addresses entered to stop spammers.
  - Scan data for spam.
 - Use a CAPTCHA optionally.
* Responses?
 - Types? HTML, JSON, files, and XML?
 - How do you handle errors? 400, 500, 404, etc.
  - Everything to the same 404 or 500 page?

## Code - frontend
* Are you going to use a framework? Or several?
 - jQuery? If so what version?
 - AngularJS?
 - React?
 - Flux?
* Include other JS from files.
* Minify
 - Javascript
 - Image optimization
 - CSS
* Folder system
* Templating
* Routing
 - Are you going to use "#" hash-bangs for anything?

## Databases
* What database system are you going to use?
* Encrypt what data in the database? Should the data be 1-way or 2-way?
 - Passwords?
 - Emails?
 - Social security numbers?
 - Credit card numbers?

## User authentication
* Login and logout
* How to store passwords
* How to reset passwords? Are you going to send users their password or have them reset it?

## Code Styling
* Use a standard like PSR-1 and PSR-2?
* Tabs or spaces? How many spaces should use you? Use tabs?
* Naming
 - Camel casing or underscore for variables and method and function names?
 - Capital or lowercase letters for variable, method, and class names?
 - Naming semantics?

## Frontend Asset Management
* How do you plan to manage images, CSS, Javascripts, files and so on?
* Files
 - Uploads? Will people be uploading to your server?
 - How do you handle file name conflicts.
 - Where do you store the files? On the server locally or remotely using something like Dropbox or Amazon Web Services?
  - If you store them locally you can't share them between your development, staging, and production
  environments easily.
 - Limit file size?
 - LImit file types and extensions?
 - Scan files for viruses?
 - How do you handle saving the URLs?
* Management with tools like npm or Bower?

## Developer Tools
* Version control system?
* Project management?
* IDE (integrated development environment)
* Log monitoring (error, access)
* Code enforcement? Make sure everyone follows code styling rules and best practices.
 - Examples: Code Climate, PHP_CodeSniffer
 - Can it change code automatically? Should it?
 - How does it warn you?
 - Code reviews?

## Monitoring
* (code) Logging system
* Monitor server(s)
 - How many servers do we need to monitor?

## Deployments
* How do you deploy your code to staging and production?

## Environment Managemant
* Use Docker?
 - Use Docker Hub, or some of the Docker Toolbox?
* Puppet, Chef, or Ansible?
* Use configuraiton management like PuphPet?
* Terraform? https://www.terraform.io/

## Environment
* Where do you store the database?
 - Its own server or spread across many?
 - Replication?
 - Remotely or locally?
* Caching system
* Operating system
 - Open source or closed source?
 - Linux or Windows?
* Use Docker?

## Security
* Use https?
* Encrypt database data?
* Need to meet any industry compliance?
 - HIPPA? For healthcare information.
 - PCI? For credit card information.
 - Do you outsource this to 3rd parties?

## Backups
* Database?
* Logs?
* Code versioning system?

## Testing
* Unit testing? PHP Unit?
* Functional testing? Are you going to test the frontend automatically?
* Do all tests have to pass before committing to master?
* Are you going to automatically test for HTTP errors on your site? 404s, 403s or 500 errors?
