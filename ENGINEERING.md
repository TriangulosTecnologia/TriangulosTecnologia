# Engineering

## Repository

We use a monorepo structure for handling all code related to a specific application. Every domain of the application is inside this repository: backend, IoT, machile learning, web and mobile applications.
This is useful because we can access any part of the application without changing the repository.

We follow [this template](https://github.com/ttoss/monorepo).

Our main programming language is Node.js with TypeScript as superset. We opt for it because it can handle the entire stack, since Lambdas from web applications.

## Development Process

It all starts with the project's Product Owner (PO). Every time we're going to start a new project, developing a new feature, or fixing a bug, the PO gives an explanation about the reason why we need to do that.
We provide the 

We've been developing a tool called calin that automates some scripts for us when we're developling an application.

## Backend

We work heavyly with cloud computing, in special using AWS.

Some services commonly used:

- Amazon DynamoDB.
- AWS AppAsync.
- Amazon Cognito.
- Amazon S3.
- AWS API Gateway.
- AWS Lambda.

### Datacube

We call Datacube a group of resorces that contains all data of our applications. We can think about this group as "If we lost some resource inside this group and if it doesn't have a backup, we lost your application."
It can be a AWS DynamoDB table, Amazon Cognito user pool, or an Amazon S3 bucket.

Our principal technology for database is DynamoBD. We always try to create applications using a single table, basically because it's serverless.
But we always consider all database options, it's depends what kind of databse is more effective for the application we're building.

## Frontend

We've chosen React.js to be our main library to build user interfaces. We've chosen it because it has a big community and we can build web, mobile, desktop, and VR applications.
It's the same idea for choosing Node.js: learn one thing, use everywhere.
