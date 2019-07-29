# Following AWS Tutorial

## [Learn to Build Full-Stack Apps with Serverless and React on AWS](https://serverless-stack.com/)

Build a full-stack production ready note taking app using Serverless and React on AWS. Follow our step-by-step open-source tutorials with screenshots and code samples.

### Run tests

### Create note

In the console:

```bash
serverless invoke local --function create --path mocks/create-event.json
```

or, if you have multiple profiles for your AWS SDK credentials:

```bash
AWS_PROFILE=myProfile serverless invoke local --function create --path mocks/create-event.json
```

### Get note

In the console:

```bash
serverless invoke local --function get --path mocks/get-event.json
```

### Get note list

In the console:

```bash
serverless invoke local --function list --path mocks/list-event.json
```
