QICI Engine Documentation for API and user manuals
=======

QICI Engine Documentation is created by [GitBook](https://github.com/GitbookIO/gitbook) using Markdown. 

You can read QICI Engine Documentation online:
- [QICI Engine Manual](http://docs.qiciengine.com/manual/index.html)
- [QICI Engine API](http://docs.qiciengine.com/api/index.html) 

### How to build

Here we use [npm-run-script](https://docs.npmjs.com/cli/run-script) to install GitBook environment and convert Markdown to html. 

For English Documentation:
```sh
npm run install-en
npm run init-en
npm run build-api-en
npm run build-manual-en
```

For Chinese Documentation:
```sh
npm run install-zh
npm run init-zh
npm run build-api-zh
npm run build-manual-zh
```

The commands above are defined in [package.json](blob/master/package.json)
```js
"scripts": {
	"install-zh": "npm install gitbook-cli && gitbook install zh/api && gitbook install zh/manual",
	"install-en": "npm install gitbook-cli && gitbook install en/api && gitbook install en/manual",
	"init-zh": "gitbook init zh/api && gitbook init zh/manual",
	"init-en": "gitbook init en/api && gitbook init en/manual",
	"build-api-zh": "gitbook serve zh/api",
	"build-manual-zh": "gitbook serve zh/manual",
	"build-api-en": "gitbook serve en/api",
	"build-manual-en": "gitbook serve en/manual"
}
```
