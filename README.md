# grunt-open

Open urls and files from a grunt task

## Usage

This is immediately useful as part of your task chain between `server` and `watch`

```js
grunt.registerTask('default', 'server open watch');
```

You can specify different configurations so that you can set up task chains like

```js
grunt.registerTask('dev', 'server open:dev watch');
grunt.registerTask('dev', 'build server open:build watch:build');
```

## Getting Started
Install this grunt plugin next to your project's [Gruntfile][getting_started] with: `npm install grunt-open`

## Configuration

This is a very simple task and takes only one configuration parameter
that can be specified under two names, `url` or `file`. They both issue
the same open command to open the destination with your system's default
application, but are useful for readability.

```js
grunt.initConfig({
  open : {
    dev : {
      url : 'http://127.0.0.1:8888/src'
    },
    google : {
      url : 'http://google.com/'
    },
    file : {
      file : '/etc/hosts'
    }
  }
})

grunt.loadNpmTasks('grunt-open');

```

[grunt]: https://github.com/gruntjs/grunt
[getting_started]: https://github.com/cowboy/grunt/blob/master/docs/getting_started.md

## Documentation

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [grunt][grunt].

## Release History

 - 0.1.0 initial releas

## License

Copyright OneHealth Solutions, Inc

Written by Jarrod Overson

Licensed under the Apache 2.0 license.
