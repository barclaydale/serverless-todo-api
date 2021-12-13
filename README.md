# todo Service built with NodeJS using Serverless Framework, running on AWS Lambda

[![Build Status](https://travis-ci.com/kraigh/serverless-todo-api.svg?branch=master)](https://travis-ci.com/kraigh/serverless-todo-api)
![Code Quality](https://sonarcloud.io/api/project_badges/measure?project=kraigh_serverless-todo-api&metric=alert_status)

![Serverless todo Service Architecture](images/sls_todo_architecture.png "Serverless todo Service Architecture")

# Running Locally

## Pre-requisites
* Install Node.js : [https://nodejs.org/en/download/](https://nodejs.org/en/download/)
* Install Serverless Framework: `npm install -g serverless`

## Get the Serverless todo Service project
* Clone Github project : [https://github.com/kraigh/serverless-todo-api](https://github.com/kraigh/serverless-todo-api)
* Alternatively, you can install the service locally from Github using the serverless command: `serverless install --url https://github.com/kraigh/serverless-todo-api`
* Install module dependencies: `npm install`

## Set-up AWS credentials
* `serverless config credentials --provider aws --key <key> --secret <secret>`
* Refer [serverless documentation](https://serverless.com/framework/docs/providers/aws/guide/credentials/) for other options.

## Test locally
* Install dynamodb local: `serverless dynamodb install`
* Start todo Service in offline mode: `serverless offline start`
* Test the REST APIs @ [http://localhost:4000](http://localhost:4000)
* Test the functions by invoking them locally. E.g. `serverless invoke local -f list`

## Deploy serverless todo service
* Deploy the todo Service to AWS Lambda: `serverless deploy`

## Test deployed functions
* Test the APIs of the deployed service using a REST client. API endpoints can be obtained using the command `serverless info`
* Or test deployed functions using `serverless invoke -f <function>`

Serverless AWS Lambda CLI Reference: [https://serverless.com/framework/docs/providers/aws/cli-reference/](https://serverless.com/framework/docs/providers/aws/cli-reference/)
