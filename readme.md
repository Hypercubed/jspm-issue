# Steps to reproduce unexpected behavior

```
cd sub
jspm install
jspm link github:sub@dev
cd ../main
jspm install
jspm install --link github:sub
```

* `"sub": "github:sub@dev"` is added to `main/config.js` as expected.
* However, neither `another` (as specified in `main/package.json` `jspm.map` section) nor `other` (as specified in `sub/package.json` `jspm.map` section) are added to `main/config.js`.
* In addition `other` is not added to `sub/config.js`.

Tested with jspm version 0.15.6.
