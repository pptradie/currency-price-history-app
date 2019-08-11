# Table of contents
[Currency Price History App by PP](#intro)
[Running the app](#running)
[Backend](#backend)
[Installing Dependencies](#running-backend-installing)
[Starting the backend app](#running-backend-starting)
[To run the backend api locally](#running-backend-local)
[To run the backend api in AWS](#running-backend-aws)
[API endpoints](#running-backend-end-points)
[Starting the frontend app](#running-frontend)
[Unit Tests](#unit-tests)
[Backend](#unit-tests-backend)
[Frontend](#unit-tests-fronend)
[Screenshots](#screenshots)
[Application](#screenshots-app)
[Unit Tests - Backend](#unit-tests-backend)
[Unit Tests - Frontend](#unit-test-frontend)

<a name="intro"/>
# Currency Price History App by PP

This is a sample app with:
* Backend - Developed as a `AWS Lambda` using `NodeJS` and `Serverless` framework.
* Frontend - Developed in `React` with `TypeScript`.
<a name="running"/>
# Running the app
<a name="running-backend"/>
## Backend
<a name="running-backend-installing"/>
### Installing Dependencies

* Install [Serverless framework](https://serverless.com/framework/docs/providers/aws/guide/installation/) - Supported versions `>=1.38.0 <2.0.0` (Tested in version `1.38.0`)

* Install NodeJs version >= 8.10
* Install npm packages - Go to the `backend` directory from the command prompt and run:

```bash
npm install
```
<a name="running-backend-starting"/>
## Starting the backend app
<a name="running-backend-local"/>
### To run the backend api locally

* Go to the `backend` directory from the command prompt and run:

```bash
# you can change port 8080 to your preferred port
serverless offline start --port 8080
```
<a name="running-backend-aws"/>
### To run the backend api in AWS
* To deploy the app to AWS: go to the `backend` directory from the command prompt and run:
```bash
serverless deploy
```
<a name="running-backend-end-points"/>
## API endpoints
		
| HTTP method | URI path | Sample Request | Sample Response
| ------ | ------ | ------ | ------ |
|`GET`|`/currency_exchange/calculate/profit?currency=<:currencyCode>`|`http://localhost:8080/currency_exchange/calculate/profit?currency=btc`|`{"currency":"BTC","date":"07-May-18","buy":{"time":"09:15 AM","price":34.98},"sell":{"time":"12:30 PM","price":37.01},"max_profit":2.04}`
<a name="running-frontend"/>
## Starting the frontend app
* Go to the `frontend` directory.
* Create `.env` file in the `frontend` directory. 
* Add below to `.env`. (There is a `.env.dist` which has all avaiable variables)
```env
NODE_PATH=src/
REACT_APP_API_HOST=http://localhost:8080
```
`REACT_APP_API_HOST` should be the host URL of the backend API.
* Run below from the command line
```node
npm start
```
* Visit http://localhost:3000/ to view the frontend App.
<a name="unit-tests"/>
# Unit Tests
<a name="unit-tests-backend"/>
## Backend
* Go to the `backend` directory from the command line and run:
```node
npm test
```
<a name="unit-tests-fronend"/>
## Frontend
* Go to the `frontend` directory from the command line and run:
```node
npm test
```
<a name="screenshots"/>
# Screenshots
<a name="screenshots-app"/>
## Application
![Application](https://prabhath-currency-data.s3-ap-southeast-2.amazonaws.com/screenshots/app.png)
<a name="unit-tests-backend"/>
## Unit Tests - Backend
![Unit Tests - Backend](https://prabhath-currency-data.s3-ap-southeast-2.amazonaws.com/screenshots/unittest-backend.png)
<a name="unit-test-frontend"/>
## Unit Tests - Frontend
![Unit Tests - Frontend](https://prabhath-currency-data.s3-ap-southeast-2.amazonaws.com/screenshots/unittest-frontend.png)


