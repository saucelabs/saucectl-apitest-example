# Authentication Examples

## What you'll find

This folder contains an example test, and is composed of the following elements:
- `README.md`: (This file) Contains the purpose of the test.
- `input.yaml`: Sets variables that will provided to test.
- `unit.yaml`: Sets the steps to perform while executing the test.

You can also get familiar with our test script syntax by following our [Synthax Documentation](https://github.com/saucelabs/saucectl-apix-example/blob/main/docs/README.md).

## Details

In this example, we make use of a variable and the `WSCrypto` extension to create a Basic Auth token.
```yaml
- id: set
  var: auth
  mode: string
  value: ${WSCrypto.base64('encode','yourUsername:yourPassword')}
```

That variable `auth` is then used in a subsequent HTTP request, which requires a Basic Authentication
```yaml
- id: get
  url: ${domain}${path}
  var: payload
  mode: json
  children:
    - id: header
      name: Authorization
      value: Basic ${auth}
```
