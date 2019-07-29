# Following AWS Tutorial

## [Learn to Build Full-Stack Apps with Serverless and React on AWS](https://serverless-stack.com/)

Build a full-stack production ready note taking app using Serverless and React on AWS. Follow our step-by-step open-source tutorials with screenshots and code samples.

## Backend - notes-app-api

### Run tests

#### Create note

In the console:

```bash
serverless invoke local --function create --path mocks/create-event.json
```

or, if you have multiple profiles for your AWS SDK credentials:

```bash
AWS_PROFILE=myProfile serverless invoke local --function create --path mocks/create-event.json
```

#### Get note

In the console:

```bash
serverless invoke local --function get --path mocks/get-event.json
```

#### Get note list

In the console:

```bash
serverless invoke local --function list --path mocks/list-event.json
```

#### Update note

In the console:

```bash
serverless invoke local --function update --path mocks/update-event.json
```

#### Delete note

In the console:

```bash
serverless invoke local --function delete --path mocks/delete-event.json
```

#### The APIs

In the console:

```bash
npx aws-api-gateway-cli-test \
--username='admin@example.com' \
--password='Passw0rd!' \
--user-pool-id='YOUR_COGNITO_USER_POOL_ID' \
--app-client-id='YOUR_COGNITO_APP_CLIENT_ID' \
--cognito-region='YOUR_COGNITO_REGION' \
--identity-pool-id='YOUR_IDENTITY_POOL_ID' \
--invoke-url='YOUR_API_GATEWAY_URL' \
--api-gateway-region='YOUR_API_GATEWAY_REGION' \
--path-template='/notes' \
--method='POST' \
--body='{"content":"hello world","attachment":"hello.jpg"}'
```

### Deploy

In the console:

```bash
serverless deploy
```

or, if you have multiple profiles for your AWS SDK credentials:

```bash
serverless deploy --aws-profile myProfile
```

to deploy only a single function (example 'list')

```bash
serverless deploy function -f list
```

#### Service Information

```bash
service: notes-app-api
stage: prod
region: eu-west-2
stack: notes-app-api-prod
resources: 35
api keys:
  None
endpoints:
  POST - https://u9pkdb1nab.execute-api.eu-west-2.amazonaws.com/prod/notes
  GET - https://u9pkdb1nab.execute-api.eu-west-2.amazonaws.com/prod/notes/{id}
  GET - https://u9pkdb1nab.execute-api.eu-west-2.amazonaws.com/prod/notes
  PUT - https://u9pkdb1nab.execute-api.eu-west-2.amazonaws.com/prod/notes/{id}
  DELETE - https://u9pkdb1nab.execute-api.eu-west-2.amazonaws.com/prod/notes/{id}
functions:
  create: notes-app-api-prod-create
  get: notes-app-api-prod-get
  list: notes-app-api-prod-list
  update: notes-app-api-prod-update
  delete: notes-app-api-prod-delete
layers:
  None
```

## Frontend - notes-app-client

### Install

```bash
npm install
```

### Run 

```bash
npm start
```
