# Serverless TODO list application

> This is initial developed for Udacity Cloud Delveloper Capstone Project

## Project Components

- RESTful API (Lambda Functions, API Gateway and DynamoDb)
- React Frontend

## How to run the application

### Deploy Backend

To deploy an application run the following commands:

```bash
cd backend
npm install
sls deploy -v
````

### Update frontend configuration

After deploying, copy the apiId from the API Gateway output and paste in the frontend config.ts

```js
# ./client/src/config.ts
const apiId = 'xgwpz39dla'
export const apiEndpoint = `https://${apiId}.execute-api.us-west-2.amazonaws.com/prod`

export const authConfig = {
  
  domain: 'koala-tree.auth0.com',                        // Auth0 domain
  clientId: 'USgkMFXki7EtgnVkZ3shj5dVMcNYaI5u',          // Auth0 client id
  callbackUrl: 'http://localhost:3000/callback'
}

```

### Frontend

```bash
cd client
npm install
npm run start
```

## Current Deplyment details

API Endpoint

```bash
https://xgwpz39dla.execute-api.us-west-2.amazonaws.com/prod/todos
```

Postman Collection

```
Udacity Cloud developer capstone.postman_collection.json
```