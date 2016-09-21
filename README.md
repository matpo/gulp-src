"# gulp-src" 
Get files or dependencies from YAML file (.yml)

Usage in gulpfile.js:
```javascript
gulp.task('source', function() {
    var sources = gulp.src('source.yml')
        .pipe(source())
        .pipe(gulp.dest('./app'));

    return gulp.src('./app/index.html')
        .pipe(inject(sources, {relative: true}))
        .pipe(gulp.dest('./app'));
});
```

And in source.yml:
```YAML
scripts:
  - node_modules/jquery/dist/jquery.min.js

#styles:
  # your stylesheet here...

# you can add any other folder
```
