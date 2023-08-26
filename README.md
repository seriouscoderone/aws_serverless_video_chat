# Serverless WebRTC Video Chat Sample

This project shows how to implement a simple Video Chat application using serverless technologies like:
- [AWS Cognito](https://aws.amazon.com/cognito/) for authentication;
- [AWS Lambda](https://aws.amazon.com/lambda/) and [AWS API Gateway](https://aws.amazon.com/api-gateway/) in the back-end;
- [AWS DynamoDB](https://aws.amazon.com/dynamodb/) as our data-store;
- [React](https://reactjs.org/) and WebRTC on the front-end;

You can get more details about this application in this [blog post](https://blog.mauriciomaia.dev/programming/video-chat/).

## Prerequisites

To compile the project, check if your environment has the following requirements installed:

1. [Node.js](https://nodejs.org/) v12.x or later
2. [npm](https://www.npmjs.com/) v5.x or later
3. [AWS CLI](https://aws.amazon.com/pt/cli/)

# Building Steps

- Install the Serverless CLI:

```bash
$ npm install -g serverless
````

- Configure a AWS profile with programatic access to the AWS API with full administrator privileges. The next command will assume the profile is called `serverless`;

- Set the environment variables inside the back-end's `serverless.yml` file;

- Deploy the application to the cloud with:

```bash
$ sls deploy --aws-profile serverless
````

- Configure the base URL of each back-end's endpoint inside the frontend's `env.ts`;

- Start the frontend with:

```bash
$ npm start
```


# Old version

First do front-end to create userpool
amplify confiugre and create IAM role etc...
amplify init (and select new environment - not default dev)
find and replace nodejs12.x with a supported version
amplify push




make sure no nvm
install n
n install 16


turn on "CloudWatch Logs for troubleshooting my API Gateway REST API or WebSocket API"
https://repost.aws/knowledge-center/api-gateway-cloudwatch-logs


endpoints:
  GET - https://yn6uyc54qe.execute-api.us-east-1.amazonaws.com/dev/contacts
  POST - https://yn6uyc54qe.execute-api.us-east-1.amazonaws.com/dev/contacts
  GET - https://yn6uyc54qe.execute-api.us-east-1.amazonaws.com/dev/user
  DELETE - https://yn6uyc54qe.execute-api.us-east-1.amazonaws.com/dev/contacts/{contactId}
  wss://4pknhwms6a.execute-api.us-east-1.amazonaws.com/dev
functions:
  AuthWS: my-video-chat-dev-AuthWS (8 MB)
  GetContacts: my-video-chat-dev-GetContacts (8 MB)
  AddContact: my-video-chat-dev-AddContact (8 MB)
  CreateUser: my-video-chat-dev-CreateUser (8 MB)
  DeleteContact: my-video-chat-dev-DeleteContact (8 MB)
  connectionHandler: my-video-chat-dev-connectionHandler (8 MB)
  defaultHandler: my-video-chat-dev-defaultHandler (8 MB)