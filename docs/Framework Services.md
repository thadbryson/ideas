
# Framework Services

## Pager
Config for "page", "page-size", and "order". Those params are passed in GET or POST and automatically read. The backend can then use that for paginating
data. Everything is session cached. So when the User comes back the paging data they last viewed is pulled back up.

**Views with standard:**
 - A table with pagination.
 - Filters with defaults.
 - Pagination links are included.
 - Sorting fields are included.

## Route Param Converter
Change route parameters with given names to entities. 
Example: {user} with value 750 would be User with ID #750. Would look up that User and pass that to the controller.

## E-mail & Messaging
 - Global Configs: Templates, template vars, to, cc, bcc.
 - Ability for attachments.

**Sending options**
 - e-mail
 - texting
 - snail mail
 - flash messages
 - internal site messages

## Rest Package
 - Return types (JSON, XML, CSV, Excel files)
 - Automap Data Domain to REST actions.

## Eloquent ORM included
 - Configuration variable for:
  - Fields on entity
  - Validation for those fields
 - Validation performed on entity
 - Load entity with Request data option.

## CMS
 - page content
 - emails
 - messages

## CLI Command
 - Output standards (text colors, headings, tables, etc)
 - Input standards (questions, choices, auto-complete, etc)

## Asset Management
 - Gulp with file
 - Bower with file

## Code Libraries
 - Unicode strings
 - Unicode arrays
 - Faker
 - Encryption
 - Codeception

## Reporting
 - Save and share SQL queries.
 - Excel and CSV exporting

## User Profiles
 - Custom user profiles saved in the database.
 - Add custom fields on the fly per project.
 - Searchable through the database.
