# babel-plugin-remove-style

Don't care about CSS in your tests? Ignore `style` props in your tests the brute force way: by removing them with the transpiler!


## Install

```shell
npm install babel-plugin-remove-style --save-dev
```

or

```shell
yarn add babel-plugin-remove-style --dev
```

## Use

In your Babel config (shown here as a `package.json` property):

```json
  "babel": {
    "env": {
      "test": {
        "plugins": [
          [ "remove-style" ]
        ]
      }
    }
  }
```

Obviously, your test runner will need to be configured to use Babel. Note that Jest agressively caches transpiled code, and might need to be run with a `--no-cache` for you to see the change after installing the plugin.
