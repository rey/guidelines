# Front end coding guidelines

## Preamble

## Prerequisites

### Sass ([Website](http://sass-lang.com))

Install Sass:

`gem install sass`

### Compass ([Website](http://compass-style.org))

Install Compass:

`gem install compass`

### Node ([Node](http://nodejs.org))

Install Node:

`brew install node`

### Grunt ([Website](http://gruntjs.com/))

Install Grunt:

`npm install -g grunt-cli`

## Getting started

## Structure

### File structure

### Folder structure

## Writing delicious Sass

### Use `.sass` syntax

* Spend more time writing code and less time pondering missing semicolons
* `.sass` file becomes super readable

### Soft tabs, 2 spaces

* Standardises `.sass` files and prevents mixing of spaces/tabs
* Prevents conflicting tab sizes
* No hidden characters in `.sass` files

Sass will spit an error due to non-standard indentation:

```
error assets/stylesheets/sass/style.sass (Line 9 of assets/stylesheets/sass/partials/_global.sass: Inconsistent indentation: 5 spaces were used for indentation, but the rest of the document was indented using 2 spaces.)
```

* Search for [How to set soft tabs in $editor](http://www.google.com/search?q=how to set soft tabs in $editor)
* Search for [How to set 2 space tabs in $editor](http://www.google.com/search?q=how to set 2 space tabs in $editor)

### Style blocks should be written in Alphabetical Order

* Any developer will know where to expect to find rules in a block
* Order out of chaos

Bad :grimacing:

``` sass
section.fish
  z-index: 10
  background-color: #ffcc00
  position: absolute
  font-family: "Futura", "Helvetica", sans-serif
  margin: $gutter
  padding: $gutter
```

Good :bowtie:

``` sass
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

Bad :grimacing:

``` sass
section.fish
  background-color: #ffcc00
  font-family: "Futura", "Helvetica", sans-serif
  margin: $gutter
  +border-radius(20px)
  padding: $gutter
  position: absolute
  z-index: 10
```

Good :bowtie:

``` sass
section.fish
  +border-radius(20px)
  background-color: #ffcc00
  font-family: "Futura", "Helvetica", sans-serif
  margin: $gutter
  padding: $gutter
  position: absolute
  z-index: 10
```
