### Hi!!👋
*This repo is a template for cypress with cucumber preproccesor*
<br/>

*The steps to configure cucumber with cypress can be found at: https://www.npmjs.com/package/cypress-cucumber-preprocessor*

**Commands that can help you**

-  npx cypress run --headed: *To run the test with video*

  

-  npx cypress run --spec **/*.features : *To run the test without video*

  

-  If u need the xpath locator: *npm install -D cypress-xpath*

  

-  For the xpath selector or other command to work, you must import it into the following file "cypress/support/e2e.js
  
```javascript
// Import commands.js using ES2015 syntax:
import './commands'
/// <reference types="cypress"** /> <--- This command us used in case you don't get the autocomplete
import 'cypress-xpath' 

// Alternatively you can use CommonJS syntax:
// require('./commands')
```

- For exceptions (Sometimes undetected exceptions appear that can invalidate the test)

```javascript
 Cypress.on('uncaught:exception', (err, runnable) => {
        return false;
 });

const url = 'https://google.com'
Given('I open Google page', () => {
  cy.visit(url)
});
```
