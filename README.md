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

## pgknexlove

## micro + pgknexlove

## React

## Typescript Types

## Typescript Derived Types / Utility Functions

## React Storybook

## React Hooks

## API Calls with React Hooks

## JSONB in SQL

## connecting via psql

## psql special commands

## npm moment library

## npm chalk library

## npm concurrently

## sqlite

## npm sqlite3 library

## Typescript project setup

## Typescript project with ttypescript

## writing README.md

## writing DEVELOPMENT.md

## Casings

PascalCase, camelCase and kebab-case. Use airbnb casing style guide.
 
## Prettier

## React Immutability and Memoization

## flexbox

## postgrest

## ms npm module

## playwright npm module

## github workflow manager

## github workflows

## npm axios

## query strings

## JSON Web Tokens

## Semantic Release

## NextJS

## Create React App

## Node fs module

## OAuth build test

## React Container vs Components

## API Copy Tests

## Bash

## Cosmic Python Architecture

## npm yargs

## Material UI

## Row Level Security

User should secure database given a schema and a query that will be used.

## Postman

## Styling Tests (match a given deisgn)

## Schema Design

## plpgsql

## Postgresql Triggers
 
## Slack Bots
