# BrowserStack Cypress CLI

### Step 1: Install the npm dependencies

```
npm install
npm link
```

### Step 2: Configuration

Fill in the `auth`, `browsers`, `run_settings` values in the `browserstack_staging.json` file to be able to run your tests. Refer to the [configuration options](https://browserstack.com/docs/automate/cypress#configure-test-run-settings) to learn more about all the options you can use in `browserstack.json` and the possible values that you can mention.
Fill in the urls as per the staging platform in `.env.k8s-platform`
Tests which will be run are inside `test/cypress-staging-tests`

### Step 3: Run your tests

After you specify the required run settings, you can run your tests on BrowserStack:

```
$ BSTACK_CYPRESS_NODE_ENV=k8s-platform browserstack-cypress run --config-file=browserstack_staging.json
```