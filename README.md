# gulp-jekyll-stream [![Build Status](https://travis-ci.org/boneskull/gulp-jekyll-stream.svg?branch=master)](https://travis-ci.org/boneskull/gulp-jekyll-stream)

> Stream a compiled Jekyll site with Gulp

**Forked from [gulp-jekyll](https://www.npmjs.com/package/gulp-jekyll)**

## Example

Example `gulpfile.js`, shown with defaults:

```js
var gulp = require('gulp');
var jekyll = require('gulp-jekyll');

gulp.task('default', function() {
  return gulp.src(process.cwd())     // where your site source lives; this is
    .pipe(jekyll({
      bundleExec: false,             // exec jekyll w/ "bundle exec"
      quiet: true,                   // suppress jekyll output; implies "--trace"
      safe: false,                   // run Jekyll in "safe" mode     
      cwd: process.cwd(),            // below paths will be relative to this
      layouts: '_layouts',           // where your layouts live
      plugins: '_plugins'            // where your plugins live
      // source: '/path/to/source'   // overrides gulp.src() above
      // destination: '_site'        // can be used instead of gulp.dest()
    ))
    .pipe(gulp.dest('_site'));
});
```

If you are using GitHub Pages with the [recommended method](https://help.github.com/articles/using-jekyll-with-pages/), then you'll want `bundleExec: true`.

## vs. `gulp-jekyll`

You'd want to use this package instead of `gulp-jekyll` if you want to pipe Jekyll's output somewhere.

The main differences are:

- You must provide a *directory path* using `gulp.src()` (or the `source` property) to the plugin; Jekyll operates on *entire directories*; not files!
- The output of this stream is all the files which Jekyll generated
- If you neglect to pipe this plugin's output, and *do not specify* the `destination` property, the generated site disappears into the ether

## Install

### Prerequisites

- Some version of [Ruby](http://www.ruby-lang.org)
- Some version of [Jekyll](http://jekyllrb.com)

```
npm install --save-dev gulp-jekyll-stream gulp
```

## History

- v0.1.0: Initial Release

## Author

[Christopher Hiller](https://boneskull.com), based on code by [Danny Garcia](http://danny-garcia.com).

## License

MIT
