
# PSRs

Frameworks are tools that help you build things. I have some ideas for patterns that usually show up in frameworks.

## Goals
 - SOA (service oriented architecture - is an architectural pattern in computer software design in which application components provide services to other components via a communications protocol, typically over a network. The principles of service-orientation are independent of any vendor, product or technology.
 - Replaceable parts

## Standards for the the following:
 - Services - Parts of a framework
 - Connections between these parts
 - Configurations - How to build these parts
 - Input - data that gets passed into the system
 - Output - structure of data that gets returned or outputted by the system

## Communication
 - HTTP
 - FTP
 - SSH
 - Command line input
 - Software arrays

## Services
 - Dependency Injection Container
 - Routing
 - Controllers with actions
 - Chains of events

## Service Models

## Events
 - Immediate calls
 - Delayed calls
 - Scheduled calls

## Views
 - Creating a view
 - Variables passed in
 - Filters on variables
 - Partials within templates

## Output
 - HTML
 - File creation
 - HTTP Responses
 - Database inserts, updates, deletes
 - Emails

## Data Models
 – All fields stored as same basic types they are in storage: a string (represents text, boolean, or a number) or null
 – Be able to identify the type of object it is.
 – Be able to identify the specific object of that type.
 – Join Models that are combinations of other models.
    – complex SQL query with many joins
    – model decorates and handles the combinations of these models

## Data Manager
 - see "Open Source.md"

## Trait Boot Methods
 - Methods that get loaded when object constructor is called.
 - Name begins with "boot".

## Router - for anything
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
