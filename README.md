# E-Commerce Backend 
> Backend API for an e-commerce site built with Node.js/Express and Postgres.
> Live demo [_here_](https://www.example.com). 

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Features](#features)
* [Setup](#setup)
* [Testing](#testing)
* [Usage](#usage)
* [Project Status](#project-status)
* [Room for Improvement](#room-for-improvement)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)


## General Information
- Backend API for an e-commerce site built with Node.js and Express
- Endpoints for shopping, authentication, user accounts, and checkout
- Provides setup for Postgres database
- Built as a learning project, feedback appreciated!


## Technologies Used
### API:
- `node.js` - version 14.17.1
- `npm` - version 8.3.0
- `express` - version 4.17.1
- `express-session` - version 1.17.2
- `http-errors` - version 1.8.1
- `jsonwebtoken` - version 8.5.1
- `stripe` - version 8.195.0
- `validator` - version 13.7.0
- `nodemon` - version 2.0.15
- `body-parser` - version 1.19.0
- `cookie-parser` - version 1.4.6
- `cors` - version 2.8.5
- `helmet` - version 4.6.0

### Database
- `psql` (PostgreSQL) - version 14.0
- `connect-pg-simple` - version 7.0.0
- `pg` (node-postgres) - version 8.7.1

### Documentation
- `swagger-jsdoc` - version 1.3.0
- `swagger-ui-express` - version 4.3.0

### Testing
- `jest` - version 27.4.3
- `supertest` - version 6.1.6
- `supertest-session` - version 4.1.0


## Features
- User accounts that allow users to store addresses and payment methods, and set a primary address and primary payment method
- Custom hashing function for passwords
- Custom authentication middleware using secure JWT
- Persistent carts that consolidate when user logs-in/registers so shopping data is not lost
- Shopping routes that allow shoppers to browse by category or search for products
- Checkout route that provides a review page before placing order
- Payment processing with Stripe
- Documentation with Swagger 


## Setup
To run locally, first create public/private key pair: 

```
node genKeyPair
```

Then create a .env file with the following fields: 

``` 
# Postgres Database
PGHOST=
PGUSER=
PGDATABASE=
PGPASSWORD=
PGPORT=

# Express server
PORT=
SESSION_SECRET=

# Node.js 
NODE_ENV='development'

# Stripe key pair 
STRIPE_PUBLIC_KEY=
STRIPE_SECRET_KEY=

# RSA key pair 
PRIV_KEY=
PUB_KEY=
```
Create an account with Stripe to generate a key pair. 
Can use a test key pair for development that will not charge cards.

The RSA key pair should contain or point to the key pair generated in the first step.

Then run the app: 

```
node index.js
```

## Testing

To run tests, first open `tests/testData.js` and add associated data fields into database. 
Update testData.js with ID values generated by database.

Once test data is added, run: 
```
npm test
```

## Usage
This project can be used as a backend for an e-commerce website. 
The project handles various endpoints a user may need to access while online shopping such as: 
- creating user accounts
- users can save addresses and payment methods to account
- displaying products and allowing query by parameter
- creating carts, and consolidating carts when a user logs in
- checkout flow and charging payments with Stripe
- order summaries accessed through user account

View full API [_here_](https://www.example.com).

## Project Status
Project is: _in progress_ 

## Room for Improvement

Room for improvement:
- Encryption of data in database
- Add more indexes to the database for faster queries

To do:
- Allow guest checkout flow
- Send confirmation email after POSTing order
- Build demo frontend site


## Acknowledgements
This project was built as part of Codecademy's Full-Stack Engineer curriculum. 
Project prompt of creating an e-commerce backend was provided by Codecademy as well as 
some helpful resources for using Express and Postgres. No starter code was provided. 

Thanks to [@zachgoll](https://github.com/zachgoll) for his **very thorough** User Authentication tutorial for working with Passport.js and building custom authentication software.
Full tutorial can be found [here](https://www.youtube.com/watch?v=F-sFp_AvHc8&list=WL&index=4&t=20087s).


## Contact
Created by [@carokrny](https://carolynkearney.me) - feel free to contact me!
