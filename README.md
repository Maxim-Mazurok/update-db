# Update Browserslist DB

<img width="120" height="120" alt="Browserslist logo by Anton Lovchikov"
     src="https://browserslist.github.io/browserslist/logo.svg" align="right">

CLI tool to update `caniuse-lite` with browsers DB
from [Browserslist](https://github.com/browserslist/browserslist/) config.

Some queries like `last 2 version` or `>1%` depends on actual data
from `caniuse-lite`.

```sh
npx update-browserslist-db
```


## Why You Need to Call it Regularly

`npx update-browserslist-db` updates `caniuse-lite` version
in your npm, yarn or pnpm lock file.

This update will bring data about new browsers to polyfills tools
like Autoprefixer or Babel and reduce already unnecessary polyfills.

You need to do it regularly for three reasons:

1. To use the latest browser’s versions and statistics in queries like
   `last 2 versions` or `>1%`. For example, if you created your project
   2 years ago and did not update your dependencies, `last 1 version`
   will return 2 year old browsers.
2. Actual browsers data will lead to using less polyfills. It will reduce
   size of JS and CSS files and improve website performance.
3. `caniuse-lite` deduplication: to synchronize version in different tools.