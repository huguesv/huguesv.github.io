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

# Adding Content

## Adding photo albums

1. Create an album in OneDrive, or some other service. Share the album, protected with a password.
1. Create a 1024 x 576 pixels jpg thumbnail file in the `assets/albums/` folder.
1. Add an entry for the album in the `_data/albums.yml` file. Albums are displayed in the order they appear in the file.

    ``` yaml
    - isVisible: true
      url: <link to the shared album>
      name: <album name>
      date: <the date appears before the album name>
      file: <thumbnail file name>.jpg
    ```

To remove an album, either remove the entry and delete the thumbnail file, or change `isVisible: false`.

## Adding home page header images

The home page shows a random image on every page load.

To add an image:

1. Create a greyscale, 960 x 320 pixels jpg file in the `assets/slider/` folder.
1. Add an entry for the image in the `_data/sliders.yml` file.

    ``` yaml
    - isVisible: true
      file: <image file name.jpg>
    ```

To remove an image, either remove the entry and delete the file, or change `isVisible: false`.

## Adding a blog entry

The home page shows a list of blog entries.

To add a blog entry:

1. Create a .markdown file in the `_posts/` folder. Entries are displayed in alphabetical order based on file name.
