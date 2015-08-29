# [gulp](https://github.com/wearefractal/gulp)-jekyll

> Compile Jekyll sites with Gulp.

**Forked from [gulp-jekyll](https://www.npmjs.com/package/gulp-jekyll) and namespaced as `@boneskull/gulp-jekyll`**

## Example

```js
var gulp = require('gulp');
var jekyll = require('gulp-jekyll');

gulp.task('default', function () {
  return gulp.src('index.html')
    .pipe(jekyll())
    .pipe(gulp.dest('./deploy/'));
});
```

## Status

## Install

Install with [npm](https://npmjs.org/package/gulp-jekyll)

```
npm install --save-dev gulp-jekyll
```

## Changelog

- v0.0.0: Initial Release

## MIT License

gulp-jekyll is freely distributable under the terms of the MIT license.

Copyright (c) 2012, Danny Garcia. All rights reserved.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/dannygarcia/gulp-jekyll/trend.png)](https://bitdeli.com/free "Bitdeli Badge")
