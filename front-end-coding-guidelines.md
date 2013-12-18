# Front end coding guidelines

## Preamble

## Technology

* Use Sass (http://sass-lang.com)
* Use Compass (http://compass-style.org)

## Folder structure

## Sass structure

## Sass blocks

### Use .sass syntax

* Spend more time writing code and less time wondering where a missed semicolon is
* `.sass` file becomes super readable

### Soft tabs, 2 spaces

* Standardises .sass files and prevents mixing of spaces/tabs
* Prevents conflicting tab sizes
* No hidden characters in .sass files

Sass will spit an error due to non-standard indentation:

```
error assets/stylesheets/sass/style.sass (Line 9 of assets/stylesheets/sass/partials/_global.sass: Inconsistent indentation: 5 spaces were used for indentation, but the rest of the document was indented using 2 spaces.)
```

* [How to set soft tabs in $editor](http://www.google.com/search?q=how to set soft tabs in $editor)
* [How to set 2 space tabs in $editor](http://www.google.com/search?q=how to set 2 space tabs in $editor)

### Style blocks should be written in Alphabetical Order

* Any developer will know where to expect to find rules in a block
* Any order in chaos is good

Bad:

```
section.fish
  z-index: 10
  background-color: #ffcc00
  position: absolute
  font-family: "Futura", "Helvetica", sans-serif
  margin: $gutter
  padding: $gutter
```

Good:

```
section.fish
  background-color: #ffcc00
  font-family: "Futura", "Helvetica", sans-serif
  margin: $gutter
  padding: $gutter
  position: absolute
  z-index: 10
```

### Mixins are called at the top of a block before regular rules

* Any developer will know where to expect to find mixins in a block
* Multiple mixins should be listed in alphabetical order

Bad:

```
section.fish
  background-color: #ffcc00
  font-family: "Futura", "Helvetica", sans-serif
  margin: $gutter
  +border-radius(20px)
  padding: $gutter
  position: absolute
  z-index: 10
```

Good:

```
section.fish
  +border-radius(20px)
  background-color: #ffcc00
  font-family: "Futura", "Helvetica", sans-serif
  margin: $gutter
  padding: $gutter
  position: absolute
  z-index: 10
```
