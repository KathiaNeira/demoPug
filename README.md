<h1>example Pug-gulp</h1>

Pug configurado con gulp 
https://github.com/pugjs/pug


```javascript
var gulp = require('gulp');
var pug = require('gulp-pug');

gulp.task('pug', function(){
  return gulp.src('./src/pug/*.pug')
  .pipe(pug({
    pretty: true
  }))
  .pipe(gulp.dest('./dist'))
})

gulp.task('pug-watch', function(){
  gulp.watch('./src/pug/*.pug', ['pug'])
});

gulp.task('default', ['pug']);
```
