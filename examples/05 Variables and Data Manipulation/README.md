# Variables and Data Manipulation

## What you'll find

This folder contains an example test, and is composed of the following elements:
- `README.md`: (This file) Contains the purpose of the test.
- `input.yaml`: Sets variables that will provided to test.
- `unit.yaml`: Sets the steps to perform while executing the test.

You can also get familiar with our test script syntax by following our [Synthax Documentation](https://github.com/saucelabs/saucectl-apix-example/blob/main/docs/README.md).

## Details

You may need to manipulate data and create partial data-structures to cover certain scenarios.  

In this example, we fetch data from a first HTTP request, then we convintiently use a variable and the JavaScript language, to obtain a new array
```yaml
- id: set
  var: productIds
  mode: lang
  lang: javascript
  body: |-
    return payload
      .filter(it => it.category === '1')
      .map(it => it.id);
```

We then walktrough this array we just created and perform subsequent operations

```yaml
- id: each
  expression: productIds
    ...
```
