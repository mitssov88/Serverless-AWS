# Serverless-AWS

[Visit the Wild Rydes website to book your Unicorn ride!](https://main.d3evvaymuqvj80.amplifyapp.com/)

## Architecture Overview

***Amazon Cognito*** manages the user pool and authenticates users.

***Amazon S3*** hosts all the HTML, CSS, and JavaScript.

***AWS Amplify*** automatically deploys all files hosted in the project root directory, thereby making it easy to deploy static websites following a CI/CD model.

Backend calls are made through an ***AWS Lambda*** function, which is also responsible for persisting data to an ***Amazon DynamoDB*** table. It's invoked by client-side JS that makes AJAX calls - for example when a user "requests a unicorn" - using ***Amazon API Gateway***.

With this configuration, the **static website turns into a dynamic web app**!
