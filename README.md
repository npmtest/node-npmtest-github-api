# npmtest-github-api

#### basic test coverage for  github-api (v3.0.0)  [![npm package](https://img.shields.io/npm/v/npmtest-github-api.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-github-api) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-github-api.svg)](https://travis-ci.org/npmtest/node-npmtest-github-api)

#### A higher-level wrapper around the Github API.

[![NPM](https://nodei.co/npm/github-api.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/github-api)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-github-api/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-github-api/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-github-api/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-github-api/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-github-api/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-github-api/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-github-api/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-github-api/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-github-api/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-github-api/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-github-api/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-github-api/build/test-report.html](https://npmtest.github.io/node-npmtest-github-api/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-github-api/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-github-api/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-github-api/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-github-api/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-github-api/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-github-api/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-github-api/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-github-api/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "github-api",
    "version": "3.0.0",
    "license": "BSD-3-Clause-Clear",
    "description": "A higher-level wrapper around the Github API.",
    "main": "dist/components/GitHub.js",
    "contributors": [
        "Ændrew Rininsland <aendrew.rininsland@thetimes.co.uk> (http://www.aendrew.com)",
        "Aurelio De Rosa <a.derosa@audero.it> (http://www.audero.it/)",
        "Clay Reimann <clayreimann@gmail.com> (http://clayreimann.me)",
        "Michael Aufreiter (http://substance.io)",
        "Mathieu Dutour <mathieu@dutour.me> (https://github.com/mathieudutour)"
    ],
    "readmeFilename": "README.md",
    "scripts": {
        "clean": "gulp clean",
        "build": "gulp build",
        "test": "mocha --opts ./mocha.opts test/*.spec.js",
        "test-coverage": "NODE_ENV=test nyc mocha --opts ./mocha.opts test/*.spec.js",
        "test-verbose": "DEBUG=github* npm test",
        "lint": "gulp lint",
        "make-docs": "node_modules/.bin/jsdoc -c .jsdoc.json --verbose",
        "release": "./release.sh",
        "codecov": "nyc report --reporter=text-lcov > coverage.lcov && codecov"
    },
    "babel": {
        "presets": [
            "es2015"
        ],
        "plugins": [
            [
                "add-module-exports",
                "transform-es2015-modules-umd"
            ]
        ],
        "env": {
            "development": {
                "sourceMaps": "inline"
            },
            "test": {
                "plugins": [
                    "istanbul"
                ]
            }
        }
    },
    "nyc": {
        "sourceMap": false,
        "instrument": false
    },
    "files": [
        "dist/*"
    ],
    "dependencies": {
        "axios": "^0.15.2",
        "debug": "^2.2.0",
        "js-base64": "^2.1.9",
        "utf8": "^2.1.1"
    },
    "devDependencies": {
        "babel-core": "^6.7.7",
        "babel-plugin-add-module-exports": "^0.2.1",
        "babel-plugin-istanbul": "3.0.0",
        "babel-plugin-transform-es2015-modules-umd": "^6.5.0",
        "babel-preset-es2015": "^6.5.0",
        "babel-register": "^6.7.2",
        "babelify": "^7.3.0",
        "browserify": "^13.0.0",
        "codecov": "^1.0.1",
        "del": "^2.2.0",
        "eslint-config-google": "^0.7.0",
        "eslint-plugin-mocha": "^4.7.0",
        "gulp": "^3.9.0",
        "gulp-babel": "^6.1.2",
        "gulp-eslint": "^3.0.1",
        "gulp-jscs": "^4.0.0",
        "gulp-jscs-stylish": "^1.3.0",
        "gulp-rename": "^1.2.2",
        "gulp-sourcemaps": "^2.2.0",
        "gulp-uglify": "^2.0.0",
        "jsdoc": "^3.4.0",
        "minami": "^1.1.1",
        "mocha": "^3.1.2",
        "must": "^0.13.1",
        "nock": "^9.0.2",
        "nyc": "9.0.1",
        "vinyl-buffer": "^1.0.0",
        "vinyl-source-stream": "^1.1.0"
    },
    "repository": {
        "type": "git",
        "url": "git://github.com/github-tools/github.git"
    },
    "keywords": [
        "github",
        "api"
    ],
    "bugs": {
        "url": "https://github.com/github-tools/github/issues"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
