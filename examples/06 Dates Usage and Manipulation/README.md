# Dates Usage and Manipulation

## What you'll find

This folder contains an example test, and is composed of the following elements:
- `README.md`: (This file) Contains the purpose of the test.
- `input.yaml`: Sets variables that will provided to test.
- `unit.yaml`: Sets the steps to perform while executing the test.

You can also get familiar with our test script syntax by following our [Synthax Documentation](https://github.com/saucelabs/saucectl-apix-example/blob/main/docs/README.md).

## Details

We use the extension `D` to generate, parse or manipulate dates.  

For instance, we may use 
```js
D.nowMillis()

> 1669286446400
``` 
to obtain the current Unix epoch in milliseconds, or
```js
D.format(milliseconds, format)
```
to format a date in a preferred Date format
```js
D.format(D.nowMillis(), 'yyyy-MM-DD HH:mm')

> 2022-11-23 10:30
```

Full documentation can be also found here: https://docs.saucelabs.com/api-testing/composer/#dynamic-dates
