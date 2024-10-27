# Personal Web Site
This web site is published to [huguesvalois.com](https://huguesvalois.com).

# How to Build
[Jekyll](https://jekyllrb.com/) is used to generate a static web site for GitHub pages.

See [Setting up a GitHub Pages site with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll) for general information.

The site uses [minima](https://github.com/jekyll/minima) as a remote theme (it is pulled from their GitHub repo instead of using a gem) since the latest version of minima has not been published to [rubygems.org](https://rubygems.org/).

## Local setup on Windows
Install Ruby 3.2 or later from [rubyinstaller.org](https://rubyinstaller.org/).

## Local build and run
1. Install dependencies with `bundle install`.
1. Generate and start the server with `bundle exec jekyll serve --livereload`.
