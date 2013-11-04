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
    ├── index.html.haml
    ├── javascripts
    │   └── all.coffee
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
- **source** - Source code. Middleman will automatically compile to /build.
