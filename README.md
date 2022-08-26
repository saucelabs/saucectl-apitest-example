# saucectl api testing example

Example running saucectl with api testing.

## What You'll Need

The steps below illustrate one of the quickest ways to get set up. If you'd like a more in-depth guide, please check out
our [documentation](https://docs.saucelabs.com/dev/cli/saucectl/#installing-saucectl).

### Install `saucectl`

```shell
npm install -g saucectl
```

### Set Your Sauce Labs Credentials

```shell
saucectl configure
```

## Running The Examples

```shell
saucectl run
```

**Note** The API project is under the SauceLabs org so you'll need to be a member of the org to run the tests.

## The Config

[Follow me](.sauce/config.yml) if you'd like to see how saucectl is configured for this repository. 

Our IDE Integrations (e.g. [Visual Studio Code](https://docs.saucelabs.com/dev/cli/saucectl/usage/ide/vscode/)) can help you out by validating the YAML files and provide handy suggestions, so make sure to check them out!
