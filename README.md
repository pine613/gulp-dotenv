# gulp-dotenv
[![npm version](https://img.shields.io/npm/v/gulp-dotenv.svg)](https://www.npmjs.com/package/gulp-dotenv)
[![Build Status](https://travis-ci.org/pine/gulp-dotenv.svg?branch=master)](https://travis-ci.org/pine/gulp-dotenv)
[![Dependency Status](https://img.shields.io/david/pine/gulp-dotenv.svg)](https://david-dm.org/pine/gulp-dotenv)
[![devDependency Status](https://img.shields.io/david/dev/pine/gulp-dotenv.svg)](https://david-dm.org/pine/gulp-dotenv#info=devDependencies)

A .env file plugin for gulp:  compiling .env to JSON

## Installation

```
$ npm install gulp-dotenv --save
```

## Usage
`.env` is a `\n` separated key-value configuration file like `KEY=VALUE`.

```js
var dotenv = require('gulp-dotenv');
var rename = require('gulp-rename');

gulp.task('dotenv', function () {
  return gulp.src('.env')
    .pipe(dotenv())
    .pipe(rename('env.json'))
    .pipe(gulp.dest('dist'));
});
```

## License
MIT &copy; Pine Mizune
