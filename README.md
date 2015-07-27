[![Pure](https://cloud.githubusercontent.com/assets/449779/5291099/1b554cca-7b03-11e4-9157-53a12d91b34a.png)](http://purecss.io)

What's Different?
-----------------

In this fork I am integrating two main features: a 12-column grid, and grid offset classes.

### 12-Column Grid

Generated form PureCSS's own [Starter Kit](http://purecss.io/start/?cols=12&prefix=.col-&sm=35.5em&md=48em&lg=64em&xl=80em#build-your-pure-starter-kit), this 12-column grid also features a more familiar and user-friendly class name: `.col`

### Grid Offset

PureCSS currently offers no solutions to offset the grid, which I consider to be a key feature in laying out content. The developers' reasoning behind this omission aside, I recognise the following workaround that uses only Vanilla PureCSS:

```html
<div class="pure-g">
    <div class="pure-u-1-3">&nbsp;</div>
    <p class="pure-u-1-3">This would be displayed in the middle third.</p>
</div>
```

I find this to be clunky and awkward, especially considering the comparable code following this implementation:

```html
<div class="pure-g">
    <p class="pure-u-1-3 pure-u-offset-1-3">This would be displayed in the middle third.</p>
</div>
```

File Naming
-----------

### Modules

* `[module]-core.css`: The minimal set of styles, ususally structural, that
  provide the base on which the rest of the module's styles build.

* `[module]-nr.css`: Rollup of `[module]-core.css` + `[module].css` +
  `[module]-[feature].css`. This is the non-responsive version of a module.

* `[module].css`: Rollup of `[module]-nr.css` + `[module]-r.css` from the
  `build/` dir. This is the responsive version of a module.
  
* `grids-responsive.css`: Unminified version of Pure's grid stylesheet which 
  includes @media queries.

* `*.min.css`: A minified file version of the files of the same name.

### Rollup Builds

* `pure.css`: A rollup of all `[module].css` files in the `build/` dir. This is
  a responsive roll-up of everything, non-minified.

* `pure-min.css`: Minified version of `pure.css` that should be used in
  production.

* `pure-nr.css`: A Rollup of all modules without @media queries. This is a
  non-responsive roll-up of everything, non-minified.

* `pure-nr-min.css`: Minified version of `pure-nr.css` that should be used in
  production.
  

Installation & Use
------------------

For Vanilla PureCSS, you can use the CDN:

```html
<link rel="stylesheet" href="http://yui.yahooapis.com/pure/0.6.0/pure-min.css">
```

Since this is lovely and custom, work it out yourself.

License
-------

This software is free to use under the Yahoo! Inc. BSD license.
See the [LICENSE file][] for license text and copyright information.


[LICENSE file]: https://github.com/yahoo/pure/blob/master/LICENSE.md
