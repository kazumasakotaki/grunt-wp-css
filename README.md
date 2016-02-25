# grunt-wp-css [![Build Status](https://travis-ci.org/cedaro/grunt-wp-css.png?branch=develop)](https://travis-ci.org/cedaro/grunt-wp-css)

> Format style sheets according to the [WordPress CSS coding standards](http://make.wordpress.org/core/handbook/coding-standards/css/).


## Getting Started

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-wp-css --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks( 'grunt-wp-css' );
```

## wpcss Task

_Run this task with the `grunt wpcss` command._


### Overview

In your project's Gruntfile, add a section named `wpcss` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
    wpcss: {
        target: {
            options: {
                commentSpacing: true, // Whether to clean up newlines around comments between CSS rules.
                config: '',           // Which CSSComb config to use for sorting properties.
            },
            files: {}
        }
    }
});
```
This task supports the file mapping format Grunt supports. Please read [Globbing patterns](http://gruntjs.com/configuring-tasks#globbing-patterns) and [Building the files object dynamically](http://gruntjs.com/configuring-tasks#building-the-files-object-dynamically) for additional details.


### Options

#### options.commentSpacing
Type: `Boolean`  
Default value: `true`  
*Optional*

Whether the plugin should attempt to automatically correct spacing around comments that appear between rule declarations within the style sheet.

#### options.config
Type: `String`  
Default value: `'default'`

The CSSComb configuration to use for sorting CSS properties. Possible values are `default` or `alphabetical`.


## Contributors

Thanks to [Gary Jones](https://github.com/GaryJones) of [Gamajo Tech](http://gamajo.com/) for researching and providing the default configuration rules, among [many other improvements](https://github.com/cedaro/grunt-wp-css/commits?author=GaryJones).


## Release History

#### 0.2.1

Updated peer dependencies to support Grunt 1.0. See [#13](https://github.com/cedaro/grunt-wp-css/pull/13)

#### 0.2.0

This is the [@GaryJones](https://github.com/GaryJones) release.

* Updated the default CSScomb config ([0887c06](https://github.com/cedaro/grunt-wp-css/commit/0887c06993c7eeea2c716d2d9ba523f3663dfa8b)).
* Updated the alphabetical CSScomb config to match improvements in the new default config.
* Fixed the exports variable name in the tests.
* Added Travis CI support.

#### 0.1.0

* Initial release.
