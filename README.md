# MPSCM Middleman Base Template

A basic resetting HTML5 template using SASS, Compass, and HAML. Rebuilt with very, very basic MPSCM-leaning styling and information (copyright, colors)

## Files

```
.
├── Gemfile
├── Gemfile.lock
├── README.md
├── config.rb
└── source
    ├── images
    │   ├── 2x
    │   │   ├── both.png
    │   │   ├── both-ko.png
    │   │   ├── scla.png
    │   │   ├── scla-ko.png
    │   │   ├── rscny.png
    │   │   └── rscny-ko.png
    │   ├── both.png
    │   ├── both-ko.png
    │   ├── scla.png
    │   ├── scla-ko.png
    │   ├── rscny.png
    │   └── rscny-ko.png
    ├── index.html.haml
    ├── javascripts
    │   ├── all.coffee
    │   └── modernizr.js
    ├── layouts
    │   └── layout.haml
    └── stylesheets
        ├── _forms.sass
        ├── _shared.sass
        └── all.sass
```
- **Gemfile** - Google ["Ruby gem"](https://www.google.com/search?q=ruby+gems)
- **Gemfile.lock** - output of `bundle install` from Gemfile.
- **README.md** - this readme.
- **config.rb** - Middleman configuration. Stuff here for how gems operate, how Middleman outputs. View the [Middleman site](http://middlemanapp.com/getting-started/#toc_5) for more information.
- **source** - Source code. Middleman will automatically compile to `/build`.
    - **images** - Images directory. Pre-stocked with logos.
        - **2x** - For retina images. Pre-stocked with hi-res logos.
    - **index.html.haml** - basic [HAML](http://haml.info)-based content area. This will be filled into the `yield` section of `source/layouts/layout.haml`.
    - **javascripts** - Where all the javascript will go. Use [Coffeescript](http://coffeescript.org) (file extension `.coffee`).
        - **modernizr.js** - a minified version of Modernizr that helps detect some current web-standard capabilities and allow for CSS and JS fallbacks when necessary. Best not to mess with this file.
    - **layouts** - Can mostly just stick to/tweak `layout.haml`, which will wrap the content from all HTML, HAML, etc in the `/source` root with a standard header, footer, CSS and Javascript tags, meta tags, jQuery, etc.
    - **stylesheets** - Best idea is to `@import` all other stylesheet files into `all.sass`, and signify as such using the underscore (`_forms.sass`, etc). Using [SASS](http://sass-lang.com). I prefer the SASS format, which does not include brackets. It's cleaner. It requires significant whitespace, which helps enforce neat code. Be careful of over-nesting (which will compile to long lines of selectors, and unneccesarily bloated files).
        - **_forms** - Basic form formatting.
        - **_shared** - A few basic colors (`$orange`,`$brown`,`$lightbeige`)