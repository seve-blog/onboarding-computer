# Onboarding Computer

## curl

Tests for curl knowledge. User should be able to implement each command in
the `tldr curl`

```
  - Download the contents of a URL to a file:
    curl http://example.com --output filename

  - Download a file, saving the output under the filename indicated by the URL:
    curl --remote-name http://example.com/filename

  - Download a file, following location redirects, and automatically continuing (resuming) a previous file transfer:
    curl --remote-name --location --continue-at - http://example.com/filename

  - Send form-encoded data (POST request of type `application/x-www-form-urlencoded`). Use `--data @file_name` or `--data @'-'` to read from STDIN:
    curl --data 'name=bob' http://example.com/form

  - Send a request with an extra header, using a custom HTTP method:
    curl --header 'X-My-Header: 123' --request PUT http://example.com

  - Send data in JSON format, specifying the appropriate content-type header:
    curl --data '{"name":"bob"}' --header 'Content-Type: application/json' http://example.com/users/1234

  - Pass a username and password for server authentication:
    curl --user myusername:mypassword http://example.com

  - Pass client certificate and key for a resource, skipping certificate validation:
    curl --cert client.pem --key key.pem --insecure https://example.com
 ```
 
 Start script should run a server. User should execute curl commands against
 that server. e.g. challenge might be...
 
 > Write the command to download a file at "http://localhost:4343/some/file.txt" to "output.txt"
 > into `challenge1.sh`

## regex

* regexone

## ssh

Run sshd in a docker container, user must copy files. Connect and do things.

Alternatively quiz user.

* ssh into a machine with a pem file
* ssh execute a command on a remote machine
* scp file back and forth

## vercel

* Deploy vercel web page that uses create react app
* Deploy NextJS app
* Deploy something with API
* Deploy API that connects to a database

## web page styling

* Mimic some web pages exactly given an image of the web page and image assets


Test each design with image diffing tools (it should exactly match)

Should have responsive challenges.

## python

Solve basic python unit tests.

## python types

Fully type a project which is not fully typed, using mypy to check where types are missing.

## knexjs

Test selecting with subqueries and insertion.

## ava tests

Should be able to write tests.

Develop tests that fail and succeed against a function in a bunch of scenarios. The grader
tests to see that certain functions fail and others succeed when ava is run. The player,
not knowing the details of the function, must implement the tests properly to get the
correct ava output.

e.g.

Write 5 tests for the function "mystery-function.js". Don't fix the tests if they fail,
but test the following things, make sure each test is named exactly as the string given
below:

* "should export default function (mysteryFunction)"
* "should also export an object mysteryObject equal to {a: 1, b: 2}"
* "await mysteryFunction("hello") should return "world"
* "await mysteryFunction(1,2) should return "three"

## micro api endpoint tests

* parse json request and perform operation on it, then return json
* add logging middleware
* handle errors with custom middleware
* handle edge cases with guard clauses

## pgknexlove

* connect to database
* connect to database at custom port/host/etc. using environment variables
* create test database in test

## micro + pgknexlove

* get database in endpoint

## React

* create todo list

player will be tested with playwright and instructed to add ids or
name fields certain ways so that playwright can figure out what to
do.

## Typescript Types

* Given a postgres schema, design a suitable type
* Type a class
* Type a function
* Type an exclusive union of top level API objects


The last point is about an exclusive (discriminate) union of top level api objects
refers to the idea that every api response is of a type, and the top level key is
enough to discriminate the content's type. e.g. We want the player to design this
or expand on an existing one given some API responses.

```
type APIResponse = HealthResponse | GetDevicesResponse

type HealthResponse = {
  HealthResponse: {
    status: "ok" | "not-online"
  }
}

type GetDevicesResponse = {
  GetDevicesResponse: {
    devices: Array<any>
  }
}
```

The validation for this can use tsc build in a strict mode. We may
have to make sure certain files haven't changed or certain imports
are still present.

You can have the grader create a temporary file or something that
tests the types. e.g. you can have a file that should throw build
errors if the object is constructed incorrectly.

## Typescript Derived Types / Utility Functions

Have the user use a bunch of the builtin typescript utility functions
as well as some of the functions in [type-fest](https://github.com/sindresorhus/type-fest)

The type-fest repo has good examples and descriptions that may help
in creating some challenges.

## React Storybook

* Add storybook to a project, make it load in all `*.stories.jsx` files
* Create stories for a bunch of different states of a component

We can validate the stories using playwright and an image diffing tool.

## React Hooks

* useState
* useEffect
* useMemo
* useRef

## API Calls with React Hooks

* API call using useState and useEffect
* API call using Apollo and GraphQL
* API call using useApi hook

I think the best way to do this might be fill in the blank or something,
it's just hard to write a validated test for.

## JSONB in SQL

* Query into a jsonb object
* Insert a JSONB record
* Query search for jsonb property list containing a string

## connecting via psql

* psql flags
* psql d command
* psql d table
* psql connect to another database
* executing basic queries

## pg_dump
  
* Dump a database to a file
* Dump a schema to a file
* Upload a schema to a database

## npm moment library

* Get current time
* Add time to a date
* Convert date to various useful formats, including fromNow

## npm chalk library

* color some terminal output
  
## npm concurrently

* write a command that builds typescript and runs a typescript server
  simultaneously and reruns on changes

## sqlite

* create a sqlite database
* use command line sqlite3 tool
* inspecting schema with .tables etc.

## npm sqlite3 library

* connect to sqlite schema
* connect to in-memory database

## Typescript project setup

* configure tsconfig, enable/disable various options

## Typescript project with ttypescript

* config absolute to relative paths conversion

## Packaging an npm library

* preparing library for publishing with "main" key in package json, scoping
* writing tests
* publishing to github packages
* automatic publishing with github workflow manager

## writing README.md

* Essential components of readme, Getting Started, Installation, Usage

## writing DEVELOPMENT.md

* Architecture, setup etc.

I think one way to test for this is to ask the player to find development
READMEs online that match the criteria (they can use github's project explore)
and provide links, we'll then validate that the READMEs match a certain regex
where it includes most of the things we want in a great development doc.

## Casings

PascalCase, camelCase and kebab-case. Use airbnb casing style guide.

* Some conversions for terms e.g. convert "get api response" to camel case.
 
## Prettier

* Prettier setup in a project
* Rewriting an entire project to format to prettier
* Setting up a prettier github workflow using github workflow manager

## React Immutability and Memoization

* Test various scenarios with questions like "what rerenders when the
  button is clicked?"

## flexbox

* Test flexbox knowledge, the player could lay out a bunch of pages
  that the grader can test with playwright

## postgrest

* Run a postgrest server
* Run a postgres server via the npm library
* Using an example schema, write tests that verify certain data is
  present (i.e. call the postgres server with axios to verify the
  data is there) the player should have to design some url queries
  to make this work

## ms npm module

* Get various times using ms

## playwright npm module

* Create a browser to perform some actions on a web page, and
  take a screenshot using playwright
  
We should make it so it's impossible to do the task on the website
without some automation. e.g. the browser has to click a button
a thousand times or something

## github workflow manager

* install various github workflows
* modify a testing github workflow to start postgres as a service

## npm axios

* make a get request
* make a post request with body and authorization header
* make a custom axios object with a base url and default authorization header

## JSON Web Tokens

* sign a jwt with a secret, parse it and verify using the secret
* sign a jwt with an private key and verify it on the other end with the public key

## Semantic Release

* test on commit standards

## NextJS

* create nextjs project with a login page, view devices page and api endpoint for login

## Create React App

* bootstrap create react app and modify to TODO list
* set up an api server and proxy to it in development mode

## Node fs module

* write a file, read a file with `fs`
* same thing with `fs/promises`

## OAuth build test

Build an OAuth system from scratch
* Two servers, a Provider and an EndProduct
* `provider/authorize` endpoint for logging in
* `end product/login` should direct to authorize
* create internal urls and stuff

We should be able to test this one with playwright, we
should pre-design the schema/database and the majority
of the server setup so that we can test against the
database for the success case.

## React Container vs Components

## API Copy Tests

## Bash

## Cosmic Python Architecture

## npm yargs

## Material UI

## Row Level Security

User should secure database given a schema and a query that will be used.

## Postman

## Schema Design

## plpgsql

## Postgresql Triggers
 
## Slack Bots
