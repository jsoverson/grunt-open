# grunt-open

Open urls and files from a grunt task

## Installation

Install using npm in the root of your project directory (where your package.json and Gruntfile.js are located)

```bash
npm install --save-dev grunt-open
```

## Usage

This is used as part of your grunt tasks, between the `server` and `watch` tasks

```js
grunt.registerTask('default', ['server', 'open', 'watch']);
```

You can specify different configurations so that you can set up task chains (see the configuration below for this example's config)

```js
grunt.registerTask('dev', ['server', 'open:dev', 'watch']);
grunt.registerTask('build', ['build', 'server', 'open:build', 'watch:build');
```

## Gruntfile Configuration

This is a very simple task and takes two configuration parameters, `path` (required) and `app` (optional). If `app` is not specified, the default system browser will be launched

```js
grunt.initConfig({
  open : {
    dev : {
      path: 'http://127.0.0.1:8888/src',
      app: 'Google Chrome'
    },
    build : {
      path : 'http://google.com/',
      app: 'Firefox'
    },
    file : {
      path : '/etc/hosts'
    }
  }
})

grunt.loadNpmTasks('grunt-open');

```

[grunt]: https://github.com/gruntjs/grunt
[getting_started]: https://github.com/cowboy/grunt/blob/master/docs/getting_started.md

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [grunt][grunt].

## Release History

 - 0.2.2 added `app` parameter.
 - 0.2.0 grunt 0.4.0 support, added and preferring `path` parameter.
 - 0.1.0 initial release

## License

Copyright OneHealth Solutions, Inc

Written by Jarrod Overson

Licensed under the Apache 2.0 license.
