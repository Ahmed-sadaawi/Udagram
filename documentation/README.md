# بسم الله الرحمن الرحيم

# Udagram:

- [Dependencies](#dependencies)

- [Environment variables](#environment-variables)

- [AWS Cloud serup:](#awscloud-serup)

- [GitHub & circleci:](#github-&-circleci)
    - [First `Build` steps:](#first-Build-steps)
    - [Deploy Steps:](#deploy-steps)

- [Testing](#testing)
    - [Unit Tests:](#unit-tests)
    - [End to End Tests:](#end-to-end-tests)

- [Built With](#built-with)


### Dependencies

```
- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- npm 6.14.8 (LTS) or more recent, Yarn can work but was not tested for this project

- AWS CLI v2, v1 can work but was not tested for this project

- A RDS database running Postgres.

- A S3 bucket for hosting uploaded pictures.

```

## Environment variables
```
POSTGRES_USERNAME = $POSTGRES_USERNAME 
POSTGRES_PASSWORD = $POSTGRES_PASSWORD 
POSTGRES_HOST     = $POSTGRES_HOST 
POSTGRES_DB       = $POSTGRES_DB 
AWS_REGION        = $AWS_REGION 
AWS_PROFILE       = $AWS_PROFILE 
JWT_SECRET        = $JWT_SECRET 
AWS_BUCKET        = $AWS_BUCKET 
AWS_ACCESS_KEY_ID = $AWS_ACCESS_KEY_ID 
AWS_SECRET_ACCESS_KEY = $AWS_SECRET_ACCESS_KEY 
PORT = 8080
URL  = $URL 

```
## AWS Cloud setup:
- RDS endpoint: database-1.c7qkyxj8hf5i.us-east-1.rds.amazonaws.com
- RDS port: 5432
- RDS name: postgres
- [S3 front-end URL: ](http://newbucket8123049.s3-website-us-east-1.amazonaws.com)
- [Elastic Beanstalk api URL: ](http://Server-env.eba-pbz5qfg5.us-east-1.elasticbeanstalk.com)

## GitHub & circleci:
The user push code to github or other platform, the github triggers circleci which is the Pipeline we used in this app.
The cicleci needs `.circleci/config.yml` file which includes all jobs and steps to run. In our case we have [build, deploy] with their steps.


### First `Build` steps:

- Sipn up environment
- Preparing environment variables
- Install Node.js 14.15
- Checkout code
- Install Frontend Dependencies
- Install API Dependencies
- Frontend build
- API Build

### Deploy Steps:

- Sipn up environment
- Preparing environment variables
- Install Node.js 14.15
- Seting Up eb cli
- Install AWS cli-latest
- configure aws access key id
- Checkout code 
- deploy App to **aws s3 bucket** and **Elastic Beanstalk**.

## Testing

This project contains two different test suite: unit tests and End-To-End tests(e2e). Follow these steps to run the tests.

1. `cd starter/udagram-frontend`
1. `npm run test`
1. `npm run e2e`

There are no Unit test on the back-end

### Unit Tests:

Unit tests are using the Jasmine Framework.

### End to End Tests:

The e2e tests are using Protractor and Jasmine.

## Built With

- [Angular](https://angular.io/) - Single Page Application Framework
- [Node](https://nodejs.org) - Javascript Runtime
- [Express](https://expressjs.com/) - Javascript API Framework

   

