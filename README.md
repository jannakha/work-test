# Welcome to UQLibrary Work Test!

These simple tasks should demonstrate your basic understanding and skills in PHP and javascript.

- read all instructions first
- implement each test (fontend and backend) in its own repo on github
- send us links to your repo when you're done

## Backend test: PHP Web Service

Construct a PHP Web Service which provides the following endpoints:

- /api/library/{id} GET 
  - takes 'id'
  - 'id' is a number
  - invalid id should return not found response
  - returns a JSON with library details (returned data can be hardcoded, loaded from local file, DB, cache, cloud service, etc)
  
- /api/library POST 
  - takes a parameter 'library' JSON representation of a library object 
  - requires an authentication token X-VALID-USER: ${token} 
  - without auth token request should return unauthorised response
  - token value can be any value for a successful response  
  - saves library data (data can be saved into a file, DB, cache, cloud service etc, etc)
     
### Sample JSON structure:
```
{
  "id":   10123, //number
  "code": "ARC100", //[3 characters 3 numbers]
  "name": "Architecture / Music Library", //string
  "abbr": "Arch Music", //string
  "url": "http://www.library.uq.edu.au/locations/architecture-music-library" //URL string
}
```

- /api/findSmallestLeaf GET takes a parameter 'tree' JSON representation of an [unsorted binary tree](https://en.wikipedia.org/wiki/Binary_tree)
 and returns a minimum value of an unsorted binary tree leaf

### Sample input:
```
{
  "root": 2,
  "left": {
    "root": 7,
    "left": {
      "root": 2
    },
    "right": {
      "root": 6
    },
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
- use a framework (Laravel, Lumen, Symfony, etc) 
- use any build tools required
- provide documentation for your services


## Frontend test: Javascript app

UQ Library provides an open API allowing users to get library data (eg library opening hours, computer availability, etc) for example:
 - http://app.library.uq.edu.au/api/library_hours - [api doc](https://github.com/uqlibrary/work-test/blob/master/api/library_hours.md)
 - http://app.library.uq.edu.au/api/computer_availability - [api doc](https://github.com/uqlibrary/work-test/blob/master/api/computers_availability.md)
 
Construct a javascript application (using AngularJS/PolymerJS/etc) allowing users to explore these objects:
- user should be able to view a list of libraries 
- user should be able to filter libraries by name
- either (or both) of these tasks:
  - user should be able to view opening hours for the selected library
  - user should be able to view available computers in the selected library 
- any other creative use of data!

### Technical requirements

- application must respond to mobile
- use a CSS framework for styling 
- should work in evergreen browsers (don't worry about IE)
- use any build tools you feel are necessary but all source code must be provided in a readable format
- an http server may be used if required

## Criteria

Your submission will be reviewed according to the following criteria:

- code quality: 
  - readablity
  - coding standards
  - comments
  - following best practices/patterns
- documentation:
  - inline comments
  - github readme
  - api documentation
- testing: provide a set of working tests (or comment how would you implement the following tests):
  - unit testing
  - 2e2 testing
  - api testing
  
## Extra credit

- provide estimation of how long would it take you to implement each mini-app, comment on how long it took you to implement it
- application deployment (provide URL to your deployed application, eg heroku, github io etc, or provide steps how to run it locally)
- comment on which tools you'd use to ensure optimised development environment
- comment on how you'd optimise your applications on server
- comment how you'd scale your applications
- comment on any issues you have come across
- which AWS services would you use for deployment of your applications or how would you deploy these applications on premise 
 


