# AngularTesting

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 17.0.10.

This is a sample project to play around with test frameworks available.
It is recommended to run the tests in a Docker container to simulate the CI environment, e.g. 
```powershell
# Run karma-compatible container
docker run --rm -it -v ${PWD}:/app trion/ng-cli-karma:17.1.3 bash
# install all packages (might be needed if previously installed on Windows)
npm ci
# run tests
npm run test-ci


# Run Node container for Jest tests
docker run --rm -it -v ${PWD}:/code node:18.19-buster bash
cd code
npm ci
npm run test-jest
```

There are 3 options I tried here:
* Karma (`npm run test`)
* jest (`npm run test-jest`)
* jest with ESM (`npm run test-esm`) - this also uses `esbuild-jest` as transformer instead of `ts-jest`, see `jest.config.mjs` file

