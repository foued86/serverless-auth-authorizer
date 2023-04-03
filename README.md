This serverless service uses Auth0 and serverless Framework for user authentication. Follow those steps to install the locally:


### 1. Clone the repository (or generate a serverless project)
```sh
sls create --name auth-service --template-url https://github.com/foued86/serverless-auth-authorizer
cd auth-service
```

### 2. Install dependencies

```sh
npm install
```

### 3. Create `secret.pem` file

This file will contain your Auth0 public certificate, used to verify tokens.

Create a `secret.pem` file in the root folder of this project. Simply paste your public certificate in there.

### 4. Deploy the stack

We need to deploy the stack in order to consume the private/public testing endpoints.

```sh
sls deploy --verbose
```

### 5. Final test

To make sure everything works, send a POST request (using curl, Postman etc.) to your private endpoint.

You can grab a test token from Auth0. Make sure to provide your token in the headers like so:

```
"Authorization": "Bearer YOUR_TOKEN"
```

You should be good to go!

<hr/>
