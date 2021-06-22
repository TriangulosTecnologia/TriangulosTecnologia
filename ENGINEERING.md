# Engineering

Hello there 👋.

This doc will explain our engineering processes, technologies that we use, and principles that guide us.

## Repository

We use a monorepo structure for handling all code related to a specific application. Every application domain is inside this repository: backend, IoT, machine learning, web, and mobile applications. Such repository structure is helpful because we can access any part of the application without changing the repository.

We follow [this template](https://github.com/ttoss/monorepo).

Our primary programming language is [**Node.js**](https://nodejs.org/en/), with [TypeScript](https://www.typescriptlang.org/) as a superset. We opt for it because it can handle the entire stack, from Lambdas to web applications.

## Development Process

We've been developing a tool named [carlin](https://carlin.ttoss.dev/) that automates some scripts for us when developing an application.

This process is being documented...

## Backend

We work heavily with cloud computing, in special using AWS. Some services that we commonly use in our applications:

- [Amazon DynamoDB](https://aws.amazon.com/dynamodb/),
- [AWS AppAsync](https://aws.amazon.com/appsync/),
- [Amazon Cognito](https://aws.amazon.com/cognito/),
- [Amazon S3](https://aws.amazon.com/s3/),
- [AWS API Gateway](https://aws.amazon.com/api-gateway/),
- [AWS Lambda](https://aws.amazon.com/lambda/)
- [Amazon CloudFront](https://aws.amazon.com/cloudfront/).

Depending on the application, we can use other services, as [Amazon Kinesis Video Streams with WebRTC](https://docs.aws.amazon.com/kinesisvideostreams-webrtc-dg/latest/devguide/what-is-kvswebrtc.html) or [AWS IoT Core](https://aws.amazon.com/iot-core/).

We follow what we call [CloudFormation Driven Development (CFNDD)](https://dev.to/ttoss/cfndd-cloudformation-driven-development-3ej9). We make cloud resources deployments by [CluodFormation](https://aws.amazon.com/cloudformation/) templates, the AWS infrastructure as code.

### Datacube

We call Datacube a group of resources that contains all data of our applications. We can think about this group as "If we lost some resource inside this group and if it doesn't have a backup, we lost your application." It can be a [Amazon DynamoDB](https://aws.amazon.com/dynamodb/) table, [Amazon Cognito](https://aws.amazon.com/cognito/) user pool, or an [Amazon S3](https://aws.amazon.com/s3/) bucket.

Our principal technology for databases is [Amazon DynamoDB](https://aws.amazon.com/dynamodb/). We always try to create applications using a single table, mainly because it's serverless. But we always consider all database options, and it depends on the kind of database that is more effective for the application we're building.

### APIs

Backend communicates with clients through APIs. [GraphQL](https://graphql.org/) API with [AWS AppSync](https://aws.amazon.com/appsync/) is our leading choice when we're building an application.

## Frontend

We've chosen [**React**](https://reactjs.org/) to be our main library to build user interfaces. We've decided to use it because it has a big community, and we can build web, mobile, desktop, VR applications, and email templates. It's the same idea for choosing Node.js: learn one thing, use it everywhere.

We used to divide our frontend applications into two parts: *UI* and *APP*.

### UI

It takes care of the design system and the basic UI components. The technologies we use here are:

- [Storybook](https://storybook.js.org/) to develop the components and document them.
- [Theme UI](https://theme-ui.com/) for theming and design system. We've chosen this library because it has a great fit with our design process, and it has a robust design specification based on [styled system](https://styled-system.com/).

### APP

It is responsible for creating the application itself. It handles API requests, routing, authentication, among others. Depending on the kind of application, we may use:

- [Next.js](https://nextjs.org/) for applications that need SEO and aren't SPA.
- [Create React App](https://create-react-app.dev/) or others like [Vite](https://vitejs.dev/) if it's a SPA.

To handle data fetching, [Relay](https://relay.dev/) is our option if we're using a GraphQL API. If it's a REST API, we choose [React Query](https://react-query.tanstack.com/).

## Testing

Testing is an indispensable step of our development process because it guarantees higher engineering costs in the future. [This article](https://arantespp.com/planning-models) shows how we evolved our development process and planning over time.

We've chosen [**Jest**](https://jestjs.io/) to be our testing framework. Jest comes in handy because it can be using on [Backend](#backend) and [Frontend](#frontend) packages. Together with Jest, we also use [React Testing Library](https://testing-library.com/docs/react-testing-library/intro) to get APIs for working with React components.
