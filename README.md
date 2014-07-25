# grunt-mocha-phantom-istanbul

> Automatically run *client-side* mocha specs via grunt/mocha/PhantomJS and support tracking code coverage with istanbul.

This is a very slight modification of [grunt-mocha](https://github.com/kmiyashiro/grunt-mocha) which only adds the capability to extract istanbul coverage data, so see [grunt-mocha](https://github.com/kmiyashiro/grunt-mocha) for usage and options.

### Settings

See [grunt-mocha](https://github.com/kmiyashiro/grunt-mocha) for all additional options that it supports.

#### options.coverage

The options for this are specified in the coverage object.

#### options.coverage.coverageFile
Type: `String`
Default: `'coverage/coverage.json'`

The file to write the coverage json data to.

Example:
```js
mocha: {
  test: {
    files: ['tests/**/*.html'],
    options: {
      coverage: {
        coverageFile: 'somePath/myCoverage.json'
      }
    }
  },
},
```

#### options.coverage.dir
Type: `String`

The directory to write a full lcov coverage report.

Example:
```js
mocha: {
  test: {
    files: ['tests/**/*.html'],
    options: {
      coverage: {
        dir: 'somePath'
      }
    }
  },
},
```

## License
Licensed under the MIT license.
