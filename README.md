# Font Awesome More 3.0.2 + SASS + Rails

With SCSS and fonts from [Font Awesome More](http://gregoryloucas.github.com/Font-Awesome-More), `font-awesome-more-sass-rails` is a gem to integrate Font Awesome More to your Rails application.

This gem was built over `font-awesome-sass-rails`, a [gem](https://github.com/littlebtc/font-awesome-sass-rails) by [Hsiao-Ting Yu](https://github.com/littlebtc).

It supports Rails 3.1.1 and older.

## Installation

Add `font-awesome-more-sass-rails` gem to your `Gemfile`:

    gem 'font-awesome-more-sass-rails'

Then add the stylesheet to your Rails assets. The simplest way to apply Font Awesome More site-wide is to add a `require` statement in `app/assets/stylesheets/application.css`:

    *= require _font-awesome-more

That's it!

If you want to manage where the stylesheet will be used or just prefer SCSS, you can use `@import` in a SCSS file (e.g. a new file named `libs.css.scss`) to import the stylesheet:

    @import 'font-awesome-more';

(By default Rails will import all SCSS files in `app/assets/stylesheets`, you can change this behavior by modifying `application.css`.)

You can also use it with the SASS-converted Bootstrap gem, like [bootstrap-sass](https://github.com/thomas-mcdonald/bootstrap-sass) or [anjlab-bootstrap-rails](https://github.com/anjlab/bootstrap-rails). Just require/import font-awesome-more right after bootstrap.

### IE7 Support

This gem also includes `font-awesome-more-ie7`, the stylesheet for IE7 support bundled with Font Awesome 3.0.

Use this stylesheet with [conditional comment](http://en.wikipedia.org/wiki/Conditional_comment) may be the best way to support IE7. But it can be difficult when it comes to assets pipeline. See this article on StackOverflow for a workaround: [Using Rails 3.1 assets pipeline to conditionally use certain css](http://stackoverflow.com/questions/7134034/using-rails-3-1-assets-pipeline-to-conditionally-use-certain-css)

When you try this workaround, in your `application-ie.css`, append:

    *= require _font-awesome-more-ie7.min

## License

The font from [Font Awesome](http://fortawesome.github.com/Font-Awesome) is under [SIL Open Font License](http://scripts.sil.org/OFL).
The SASS & CSS from [Font Awesome](http://fortawesome.github.com/Font-Awesome) is under the [MIT License](http://opensource.org/licenses/mit-license.html).

Others are under MIT license.
