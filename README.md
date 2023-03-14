# Overview

This repository is a serverless webapp demo deployed on AWS, following [these](https://aws.amazon.com/getting-started/hands-on/build-serverless-web-app-lambda-apigateway-s3-dynamodb-cognito/module-3/) instructions. It is a fictional rideshare platform that allows users to register and request unicorn rides from any location. 

It is deployed via AWS amplify, handles user accounts via cognito, and uses a serverless lambda backend to query a dynamo database, assigning unicorns to each "job".
#
# Usage

The webapp is live and can be accessed via:

[wildrydes-site](https://master.d1lp0ew62r5h9w.amplifyapp.com/)
-

#
# Architecture

This repo contains the content of the webpage, provided by AWS [here](https://aws.amazon.com/getting-started/hands-on/build-serverless-web-app-lambda-apigateway-s3-dynamodb-cognito/module-1/). 

The architecture is as follows:

<p align="left">
  <img src="./docs/IMG/architecture_aws.png" alt="Spectrum" width="1024">
  <br />
</p>
<p align = "right">
( schematic via AWS )
</p>

- The static components of the webapp are deployed via Amplify. 

- Cognito is used to manage the user pool and authentication. Upon registering, the user provides an email address (optional), and is sent a verification code. 

- A RESTful API allows queries to be conducted via Lambda against a DynamoDB database of "available" unicorns, assigning one to each user request. 

- Mapping functionality is established via ArcGIS. 









