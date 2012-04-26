# grunt-mocha

(package/README format heavily borrowed from [grunt-jasmine-task](https://github.com/jzaefferer/grunt-css) and builtin QUnit task)

[Grunt](https://github.com/cowboy/grunt) plugin for running Mocha browser specs in a headless browser (PhantomJS)

## Getting Started

### Grunt and this plugin
Install this grunt plugin next to your project's [grunt.js gruntfile](https://github.com/cowboy/grunt/blob/master/docs/getting_started.md) with: `npm install grunt-mocha`

Then add this line to your project's `grunt.js` gruntfile at the bottom:

```javascript
grunt.loadNpmTasks('grunt-mocha');
```

Also add this to the ```grunt.initConfig``` object in the same file:

```javascript
mocha: {
  index: ['specs/index.html']
},
```

Replace ```specs/index.html``` with the location of your mocha spec running html file.

Now you can run the mocha task with `grunt mocha`, but it won't work. That's because you need...

### PhantomJS

This task is for running Mocha tests in a headless browser, PhantomJS. [See the FAQ on how to install PhantomJS](https://github.com/cowboy/grunt/blob/master/docs/faq.md#why-does-grunt-complain-that-phantomjs-isnt-installed).

### Mocha

You also need to have Mocha included and called inside your spec html file. This task does not do that for you, please do it yourself. If you do not know what I am talking about, how did you find this page?

You must also write tests. How much detail do I need to give here?

### Hacks

The PhantomJS -> Grunt superdimensional conduit uses `alert`. If you have disabled or aliased alert in your app, this won't work. I have conveniently set a global `PHANTOMJS` on `window` so you can conditionally override alert in your app.

## License
Copyright (c) 2012 Kelly Miyashiro
Licensed under the MIT license.