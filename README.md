# saucectl api testing example

Example running saucectl with api testing.

## What You'll Need

- The steps below illustrate how to get set up. If you'd like a more in-depth guide, please check out
our [documentation](https://docs.saucelabs.com/dev/cli/saucectl/#installing-saucectl).
- You can also get familiar with our test script syntax by following our [documentation](https://github.com/saucelabs/saucectl-apitest-example/blob/main/docs/README.md).

### Install `saucectl`

```shell
npm install -g saucectl
```

### Set Your Sauce Labs Credentials

```shell
saucectl configure
```

## Running The Examples

**Note:** A Project needs to be existing in your account with the `saucectl-apitest-example` name.

```shell
saucectl run
```

#### Exit code

`saucectl` will give a non-zero exit code if any of the tests fail. Otherwise, it will be returning 0.

### Test results
You will have a summary of the test results along with the test duration of each test.

## The Config

[Follow me](.sauce/config.yml) if you'd like to see how saucectl is configured for this repository. 

Our IDE Integrations (e.g. [Visual Studio Code](https://docs.saucelabs.com/dev/cli/saucectl/usage/ide/vscode/)) can help you out by validating the YAML files and provide handy suggestions, so make sure to check them out!
