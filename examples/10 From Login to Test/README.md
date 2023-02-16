# From Login to Test

## What you'll find

This folder contains an example test, and is composed of the following elements:
- `README.md`: (This file) Contains the purpose of the test.
- `input.yaml`: Sets variables that will provided to test.
- `unit.yaml`: Sets the steps to perform while executing the test.

You can also get familiar with our test script syntax by following our [Synthax Documentation](https://github.com/saucelabs/saucectl-apix-example/blob/main/docs/README.md).

## Details

In this example we cover a complete testing scenario, starting with an authentication, with an access token exchange and then some subsequent HTTP requests + operations/assertions over the obtained payloads.

First, a first request to the authentication API endpoint is made
```yaml
- id: post
  url: ${domain}${authenticationPath}
  var: loginPayload
  mode: json
  children:
    - id: header
      name: key
      value: ${key}
    - id: body
      contentType: application/json
      content: |-
        {
          "user": "${username}",
          "password": "${password}"
        }
```

The access token is retrieved inside the authentication response payload and conveniently saved into a variable
```yaml
  - id: set
    var: accessToken
    mode: string
    value: ${loginPayload.Token}
```

Then, the `accessToken` variable can be used in subsequent HTTP requests, which require such authentication token
```yaml
- id: get
  url: ${domain}${cartPath}
  var: cartPayload
  mode: json
  children:
    - id: header
      name: usertoken
      value: ${accessToken}
```
