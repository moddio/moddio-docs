# How our documentation works

This entire documentation is produced from this github repo (https://github.com/moddio/moddio-docs)
Merging PR's in there will update this documentation immediately.

# Running documentation in a local machine

We use [docsify](https://docsify.js.org/#/) as a framework for our docs.

For local development and testing, it is best to use the `docsify-cli` package, which allows you to easily view changes on `localhost:3000`. The following example uses `npm` with the `-g` flag for a global install from the command line.

```sh
npm i docsify-cli -g
```

To run our doc locally, clone [our repo](https://github.com/moddio/moddio-docs) and typing below inside moddio-docs/ folder:

```sh
docsify serve
```

The changes will reflect immediately after saving the files. There is no need to restart the docsify server. 