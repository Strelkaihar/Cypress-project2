# Cypress Test Cases for Project 2

This repository contains Cypress test cases for the login functionality of Project 2.

## Prerequisites

Before running the test cases, make sure you have the following:

- [Node.js](https://nodejs.org/) installed
- [Cypress](https://docs.cypress.io/guides/getting-started/installing-cypress.html#System-requirements) installed


## Installation

1. Clone this repository:

```bash
git clone git@github.com:Strelkaihar/Cypress-project2.git
```
2. Navigate to the project folder:

```bash
cd Project_2
```
3.Install dependencies:
```bash
npm install
```

### Usage

To modify or extend the Cypress configuration, edit the `cypress/config.js` file according to your project's requirements.


```javascript
// cypress/config.js

const { defineConfig } = require("cypress");

module.exports = defineConfig({
  viewportHeight:1080,
  viewportWidth: 1980,
  chromeWebSecurity: false,
  retries: 1,
  e2e: {
    setupNodeEvents(on, config) {
      // implement node event listeners here
    },
    specPattern: 'cypress/e2e/integration/*.cy.{js,jsx,ts,tsx}',
  },
});
```
## Running the Tests with Configuration
When running the Cypress tests, the configuration data from example.json will be used to perform the test scenarios. Ensure that the data in example.json is accurate and represents the test environment.
## Pages

The `Pages` folder contains the `LoginPage.js` file, which serves as a page object for the login functionality in Project 2. This page object helps organize and centralize the interactions with the different elements on the login page.

## Running the Tests
To run the Cypress tests, use the following command:
```bash
npm cypress run
```
or run with a browser (Chrome preffered)
```bash
npm cypress open
```