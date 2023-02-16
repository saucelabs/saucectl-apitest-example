# Test Data Generation

## What you'll find

This folder contains an example test, and is composed of the following elements:
- `README.md`: (This file) Contains the purpose of the test.
- `input.yaml`: Sets variables that will provided to test.
- `unit.yaml`: Sets the steps to perform while executing the test.

You can also get familiar with our test script syntax by following our [Synthax Documentation](https://github.com/saucelabs/saucectl-apix-example/blob/main/docs/README.md).

## Details

The extension `F` is useful to generate test (fake) data.  

For instance, we can use
```js
F.phone()
```
to obtain a randomly generated phone number

or
```js
F.zipCode()
```
to obtain a generated zip code.



These are just a few examples of what you can do by using the `F` extension.
A full documentation can be found here: https://docs.saucelabs.com/api-testing/composer/#generating-test-data
