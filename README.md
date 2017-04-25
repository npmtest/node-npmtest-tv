# npmtest-tv

#### basic test coverage for  [tv (v6.1.0)](https://github.com/hapijs/tv#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-tv.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-tv) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-tv.svg)](https://travis-ci.org/npmtest/node-npmtest-tv)

#### Interactive debug console plugin for hapi

[![NPM](https://nodei.co/npm/tv.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/tv)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-tv/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-tv/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-tv/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-tv/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-tv/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-tv/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-tv/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-tv/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-tv/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-tv/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-tv/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-tv/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-tv/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-tv/build/test-report.html](https://npmtest.github.io/node-npmtest-tv/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-tv/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-tv/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-tv/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-tv/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-tv/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-tv/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-tv/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-tv/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/hapijs/tv/issues"
    },
    "dependencies": {
        "backbone": "1.3.x",
        "bootstrap": "3.3.x",
        "chance": "1.0.x",
        "handlebars": "4.0.x",
        "hbsfy": "2.7.x",
        "hoek": "4.x.x",
        "jquery": "3.1.x",
        "json-markup": "1.1.x",
        "lodash": "4.17.x",
        "moment": "2.17.x",
        "ws": "1.1.x",
        "zeroclipboard": "2.3.x"
    },
    "description": "Interactive debug console plugin for hapi",
    "devDependencies": {
        "babel-preset-es2015": "6.18.x",
        "babelify": "7.3.x",
        "browserify": "13.3.x",
        "browserify-istanbul": "2.0.x",
        "chai": "3.5.x",
        "chai-jquery": "2.0.x",
        "code": "4.x.x",
        "es5-shim": "4.5.x",
        "hapi": "11.x.x",
        "inert": "4.x.x",
        "istanbul": "0.4.x",
        "lab": "11.x.x",
        "mocha": "3.2.x",
        "mocha-phantomjs": "4.1.x",
        "node-sass": "4.3.x",
        "onchange": "3.2.x",
        "phantomjs-prebuilt": "2.1.x",
        "sinon": "1.17.x",
        "sinon-chai": "2.8.x",
        "vision": "4.x.x",
        "watchify": "3.8.x"
    },
    "directories": {},
    "dist": {
        "shasum": "336bab248ce84e709fedd4b73321196b1e0fecff",
        "tarball": "https://registry.npmjs.org/tv/-/tv-6.1.0.tgz"
    },
    "engines": {
        "node": ">=4.0.0"
    },
    "gitHead": "02534fe2d701d37e5108488e6bfafa6e22d8bf8d",
    "homepage": "https://github.com/hapijs/tv#readme",
    "keywords": [
        "debug",
        "console",
        "hapi",
        "plugin"
    ],
    "license": "BSD-3-Clause",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "hueniverse"
        },
        {
            "name": "wyatt"
        },
        {
            "name": "cjihrig"
        },
        {
            "name": "osukaa"
        }
    ],
    "name": "tv",
    "optionalDependencies": {},
    "peerDependencies": {
        "hapi": ">=11.x.x",
        "inert": ">=4.x.x",
        "vision": ">=4.x.x"
    },
    "repository": {
        "type": "git",
        "url": "git://github.com/hapijs/tv.git"
    },
    "scripts": {
        "boot": "node examples/simple.js",
        "build": "npm run build-js && npm run build-styles && npm run build-test && npm run copy-fonts && npm run copy-assets",
        "build-js": "browserify -t hbsfy -e source/js/app.js source/js/**/*.js > public/js/main.js -d",
        "build-styles": "node-sass source/styles/style.scss public/css/style.css",
        "build-test": "browserify -t [ babelify --presets [ es2015 ] ] -t hbsfy -t [ browserify-istanbul --ignore **/*.hbs ] test/client/main.js -o test/bundle.js",
        "copy-assets": "cp -R vendor/ZeroClipboard.swf public/js",
        "copy-fonts": "cp -R source/fonts/vendor/bootstrap/** public/fonts",
        "post-js": "WATCH=true onchange test/bundle.js -w -d 1000 -- npm run test",
        "prepublish": "npm run build",
        "pretest": "[ -z \"$WATCH\" ] && npm run build-test || true",
        "start": "npm run build && npm run boot",
        "start-dev": "npm run watch & npm run boot",
        "test": "mocha-phantomjs -p node_modules/.bin/phantomjs test/client/index.html --hooks test/client/phantomHooks.js && lab test/index.js -a code -t 100 -L",
        "test-client-cov": "npm run test && istanbul report --root coverage lcov",
        "watch": "npm run build && npm run watch-js & npm run watch-test & npm run watch-styles & npm run post-js",
        "watch-js": "watchify -t hbsfy -e source/js/app.js source/js/**/*.js -o public/js/main.js -d -v",
        "watch-styles": "node-sass source/styles/style.scss public/css/style.css -w source/styles -r",
        "watch-test": "watchify -t hbsfy -e test/client/main.js test/client/**/*.js -o test/bundle.js -d -v"
    },
    "version": "6.1.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
