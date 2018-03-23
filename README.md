### Setting up Ionic Testing

## To use in cooper challenge
- copy the `e2e` and `test-config` folders to your projects root
- need to install some dependencies
    ```
    npm install --save-dev angular2-template-loader html-loader jasmine jasmine-spec-reporter
    karma karma-chrome-launcher karma-jasmine karma-jasmine-html-reporter karma-sourcemap-loader
    karma-webpack karma-coverage-istanbul-reporter istanbul-instrumenter-loader null-loader
    protractor ts-loader ts-node @types/jasmine @types/node
    ``
- add these scripts to the `scripts` node in `package.json`
    ```
    "test": "karma start ./test-config/karma.conf.js",
    "test-ci": "karma start ./test-config/karma.conf.js --single-run",
    "test-coverage": "karma start ./test-config/karma.conf.js --coverage",
    "e2e": "npm run e2e-update && npm run e2e-test",
    "e2e-test": "protractor ./test-config/protractor.conf.js",
    "e2e-update": "webdriver-manager update --standalone false --gecko false"
    ```
- Copy the `app.component.spec.ts` file into `src/app` folder
- You need to extract `this._tokenService.init` `this.initializeApp` and `this.pages` from constructor to a method called  `ngOnInit`
- run npm install
- run npm run test
- if you get `typescript` incompatible errors you need to update your dependencies in package.json with the ones in `for package json.txt` file
