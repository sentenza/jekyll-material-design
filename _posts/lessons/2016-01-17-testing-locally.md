---
layout: post
category : lessons
tagline: "How to test your Jekyll site locally"
tags : [intro, beginner, jekyll, tutorial]
---
{% include JB/setup %}

In this tutorial I will teach you *how to test your Jekyll Bootstrap3* site locally.

Jekyll is a parsing engine bundled as a ruby gem used to build static websites from
dynamic components such as templates, partials, liquid code, markdown, etc. Jekyll is known as "a simple, blog aware, static site generator".

To test your site locally, you'll need

- [ruby](https://www.ruby-lang.org/en/)
- [Jekyll](https://http://jekyllrb.com/)
- [github-pages](https://github.com/github/pages-gem) gem

<!--more-->

### Installing ruby

There are
[lots of different ways to install ruby](https://www.ruby-lang.org/en/installation/).


In Mac OS X, older versions of ruby will already be installed.  But I
use the [Ruby Version Manager (RVM)](http://rvm.io/) to have a more
recent version.  You could also use [Homebrew](http://brew.sh/).

In Windows, use [RubyInstaller](http://rubyinstaller.org/). (In most
of this tutorial, I've assumed you're using a Mac or some flavor of
Unix. It's possible that none of this was usable for Windows
folks. Sorry!)


### Installing the github-pages gem

Run the following command:

    gem install github-pages

This will install the `github-pages` gem and all dependencies
(including [jekyll](http://jekyllrb.com/)).

Later, to update the gem, type:

    gem update github-pages


### Testing your site locally

To construct and test your site locally, go into the directory and
type

    jekyll build

This will create (or modify) a `_site/` directory, containing
everything from `assets/`, and then the `index.md` and all
`pages/*.md` files, converted to html. (So there'll be
`_site/index.html` and the various `_site/pages/*.html`.)

Type the following in order to &ldquo;serve&rdquo; the site.
This will first run `build`, and so it does _not_ need to be
preceded by `jekyll build`.

    jekyll serve

To make jekyll automatically re-build your changes you can also add the `--watch` option:

    jekyll serve --watch

Now open your browser and go to <http://localhost:4000>.

Read the complete tutorial on <http://jekyllrb.com/docs/usage/>.

## License

[MIT](http://opensource.org/licenses/MIT)
