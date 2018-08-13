# Welcome to UQLibrary Work Test!

These simple tasks should demonstrate your basic understanding and skills in PHP and JavaScript.
- there's no time limit on the test
- read all instructions first
- implement each test (frontend and backend) in its own public repo on github/bitbucket/etc
- commit often to view your work progress
- send us links to your repo when you're done

## Backend test: PHP Web Service

Construct a PHP Web Service which provides the following endpoints:

- /v1/library/{id} GET 
  - takes 'id'
  - 'id' is a number
  - invalid id should return not found response
  - returns a JSON with library details (returned data can be mocked, hardcoded, loaded from local file, DB, cache, cloud service, etc)
  
- /v1/library POST 
  - takes a parameter 'library' JSON representation of a library object 
  - requires an authentication token X-VALID-USER: ${token} 
  - without auth token request should return unauthorised response
  - token value can be any value for a successful response  
  - saves library data (data doesn't have to be saved (just demonstrate Model layer), but you can save it into a file, DB, cache, cloud service etc, etc)
     
### Validation rules:
- 'id' is a positive number
- 'code' is a 3 character, 3 number combination ARC101
- 'name' is a string
- 'abbr' is a string
- 'url' is a valid URL

### Sample JSON structure:
```
{
  "id":   10123, 
  "code": "ARC100", 
  "name": "Architecture / Music Library", 
  "abbr": "Arch Music", 
  "url": "https://web.library.uq.edu.au/locations-hours/architecture-music-library" 
}
```

- /v1/findSmallestLeaf GET takes a parameter 'tree' JSON representation of an [unsorted binary tree](https://en.wikipedia.org/wiki/Binary_tree)
 and returns a minimum value of an unsorted binary tree leaf. Leaf is a tree element which doesn't have any children.

### Sample input:
```
{
  "root": 1,
  "left": {
    "root": 7,
    "left": {
      "root": 2
    },
    "right": {
      "root": 6
    }
  },
  "right": {
    "root": 5,
    "left": {
      "root": 9
    }
  }
}
```

### Sample output:
2


### Technical requirements
- use a framework: Laravel 5 (preferred), Lumen, Symfony, etc
- use any build tools required
- provide documentation for your services


## Frontend test: Javascript app

UQ Library provides an open API allowing users to get library data (eg library opening hours, computer availability, etc) for example:
 - https://api.library.uq.edu.au/v1/library_hours - [api doc](https://github.com/uqlibrary/work-test/blob/master/api/library_hours.md)
 - https://api.library.uq.edu.au/v1/computer_availability - [api doc](https://github.com/uqlibrary/work-test/blob/master/api/computers_availability.md)
 
Construct a javascript application (preferably using ReactJS and Redux) allowing users to explore these objects:
- user should be able to view a list of libraries 
- user should be able to filter libraries by name
- either (or both) of these tasks:
  - user should be able to view opening hours for the selected library
  - user should be able to view available computers in the selected library 
- any other creative use of data!

### Technical requirements

- application must be delivered using responsive design (mobile/tablet/desktop)
- use a CSS framework for styling eg Material UI (default Bootstrap look and feel is fine too)
- should work in evergreen browsers (don't worry about IE)
- use any build tools you feel are necessary but all source code must be provided in a readable format
- an http server may be used if required
- use a Javascript framework: ReactJs + Redux (preferred), with MaterialUI/other material libraries

## Criteria

Your submission will be reviewed according to the following criteria:

- code quality: 
  - readability
  - coding standards
  - following best practices/patterns
- documentation:
  - inline comments
  - github readme
  - api documentation
  - instructions on how to run api/javascript app
- testing: provide a set of working tests (or comment how would you implement the following tests):
  - unit testing
  - e2e testing
  - api testing
  
## Questions to answer

- provide estimation of how long would it take you to implement each mini-app, comment on how long it took you to implement it
- application deployment (provide URL to your deployed application, eg heroku, github io etc, or provide steps how to run it locally)
- comment on which tools you'd use to ensure optimised development environment
- comment on how you'd optimise your applications on server
- comment how you'd scale your applications
- comment on WCAG 2.0 AA compliance considerations
- comment on SEO considerations
- comment on any issues you have come across
- which AWS services would you use for deployment of your applications or how would you deploy these applications on premise