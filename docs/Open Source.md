
# Open Source Projects

## Unit Test Creation Framework
- Reflection to read classes and function names and annotations
- Create Mock and Stub classes
- Create unit testing functions for all public methods and parameters on classes.
- Create factories for objects

## Hosting Library Abstraction
- Abstraction between different hosting services (AWS, Linode, Rackspace, SoftLayer, Heroku, etc)
- Migrate easily between different services

## Drunk Test to prevent website & app access - Chrome Extension & Mobile App
﻿- Block access to certain sites when you're drunk
- Block access to certain apps when you're drunk
- Enable for certain date and times
- Test to unlock app/site

## Chain
 - Chain classes together to modify variables.
 - Will run SPL functions by default.
 - Variable to be modified is ALWAYS 1ST ARGUMENT.
 - Collection Pipeline functionality.

**Chain types**
 - Strings (stringy package?)
 - Arrays
 - Numbers (integers, floats)
 - File paths
 - Money
 - Internet protocols
 - Validation (credit cards, Internet addresses, etc)
 - Casting (one variable type to another)

## Money Pattern object type
- by Martin Fowler (Value/Unit Pairing)
- Library with classes for unit value types.
- Currency, measurements (cm, ft, in, etc)

## Form Security
- Scrub bad data (SQL injection attacks, XSS attacks)
- CSRF protection
- flood protection

## Convention Enforcement
- Scan code for non-standard styling
- Enforce PSRs

## Object God
- Reflection on classes (methods, properties)
- Attach methods to run before and after other methods are called.
- Attach repetitive methods onto objects.

## Web Scan
- Scan a domain and perform tasks on each URL.

## Sticky Vars
- Save variables submitted (form, POST, GET, command line, etc) to be defaults later.
- Statistics on submitted variables
- Use Doctrine/Cache project.
- Add caching for Sessions and PDO.

## Data Domain
- Collections
- Standards for entities
- forms
- creating form views
- Standards of Structure and Relationships of Data

## Database Versioning
- Get schema configuration to get database versioning.
- Don't use arbitrary number schemes.

## On Page CMS
- CMS components on the actual content page itself.
- Icons show for editing actions
- Change post content - WYSIWYG
- Image and file upload for edit
- Menu items add, remove, update
- jQuery plugin
- Save to back end database

## Info Bomb
- Site to upload content to as many destinations as possible
- Useful for:
    - Whistle blowing
    - Getting the word out to as many people as possible
    - Broadcasting information when you're in danger
- Destinations: Facebook, Twitter, YouTube, WikiPedia, WikiLeaks, Tumbler, WordPress, Blogger, Google+, Email, Snail mail

## Filesystem directory with tags
 - File types: images, text files
 - Show/hide based on selected tags

## No Login System
 - Site can login automatically by checking the client device.
 - Passes back User data automatically.
 - ID number
 - Token for login
 - Users are anonymous.
 - Sites may interact with User.
 - User must give permission.
 - Site is not given identifiable information from that.
 - Services
   - Email User
   - Contact User's friends
   - Get friends list (friends' IDs)
   - Likes and dislikes

## Lego Web Components - Standards
 - Switchable 3rd party web components that can go on your site
 - Width/height/depth
 - Theming
  - colors
  - fonts
  - show or hide elements
  - API for adjusting code
  - URLs for actions

## Global Functions - PHP
 - cast::configure(array $config);
  - Configure the casting library.
  - Integers - decimals to round up or down.
 - cast::{type}($value);
  - Cast the $value to the specific type.
  - integer() - strings to integers. Decimals round up or down by configuration.
  - string()
  - convert to string. Call __toString() on objects.
  - Blank strings to null. Configure option.

## Version Control System With Custom Paths
 - Version control system
 - Ability to add any file path or directory to your project
 - Even paths outside the project path

## Anything Router
 - Match any type of input to a pattern route. Then Execute code from it.
 - Route
  - string $pattern: String for the pattern to match.
  - GET /user/1 => GET /user/{id}
  - POST /user/1/auth => POST /user/{id}/auth
  - GET /user/*/something => GET /user/1/something, GET /user/2/something, GET /user/1/2/3/a/abc/~/something
  - array $aliases[]: to the $pattern
  - array $callbacks[]: array of Closures or strings (saved closures) to call.
  - array $params[]: parameters for the pattern.
  - Array of values (param name)
  - Key (name) => values (validation for the parameter)
  - ->route(string $pattern, array|Closure|null|false $callbacks); // Add route
  - $callbacks is array: Callbacks to run on run().
  - Closure: Run just this Closure on run()
  - null: Do nothing. Just return true/false for pattern being found.
  - false: remove route
  - ->alias(string $pattern, string $alias); // Add alias to pattern
  - ->run(string $find, array $params = []); // Find route and execute all callbacks. Return result.
  - ->save(string $find, array $params = []); // Delay run of find until ->flush() called.
  - ->flush(); // Run and return all saved finds
  - ->getRoute(string $pattern); // Find route and return Route object.
  - ->getRouteByFind(string $find); // "" with Find string
  - ->getRouteByAlias(string $alias); // "" with alias string

## Error Reporting
 - Log errors with Monolog
 - Scan error logs for reports
 - Alert for errors: texts, emails, etc
 - Suggest possible solutions for errors
 - Match text of errors
 - Link to Stack Overflow

## Santa's Workshop
Content generator (files and directories) from templates. Creates **file content** as well.

## Data Manager Interface
 - Standard for wrapping data systems (ORMs, DBAL, etc).
 - Methods:
  - build(array $fields, $className = null)
  - export(BaseEntity $entity, $type = 'array')
   - json
   - xml
   - csv
   - file (Excel, CSV)
  - form($formName, $className = null)
  - isValid(BaseEntity $entity)
   - Return true/false for validation
  - getErrors()
   - Return array of errors for object.
