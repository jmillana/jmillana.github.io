---
layout: single
title:  "Setting up GitHub Pages from scratch"
date:   2022-09-30 19:24:52 +0200
categories: jekyll update
---
This post is a step-by-step guide on how to set up a GitHub Pages site from scratch. It is based on the [official documentation](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll) and the [Jekyll docs](https://jekyllrb.com/docs/).

## Prerequisites
* GitHub account: to create a new repository [official documentation](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll)
* Ruby and RubyGems: to install Jekyll and Bundler [official documentation](https://jekyllrb.com/docs/installation/)
* Jekyll and Bundler: to create a new Jekyll site [official documentation](https://jekyllrb.com/docs/)

## Step 1: Create a new Jekyll site

To create a new Jekyll site, you can use the `jekyll new` command. This command will create a new Jekyll site in the current directory. If you want to create a new Jekyll site in a different directory, you can use the `--path` option. For example, if you want to create a new Jekyll site in a directory called `my-site`, you can use the following command:

```bash
jekyll new --skip-bundle .
```

## Step 2: Add a theme (minimal-mistakes)
Add `minimal-mistakes` theme to your site's `Gemfile` by creating/replacing the following contents:

```ruby
source "https://rubygems.org"

gem "github-pages", group: :jekyll_plugins
gem "jekyll-include-cache", group: :jekyll_plugins
```
Add `jekyll-include-cache` plugin to your site's `_config.yml`
```yaml
Then, run `bundle` to install the theme.

Set the `theme` in your site's `_config.yml` to enable it:
```yaml
# Theme
remote_theme           : "mmistakes/minimal-mistakes@4.24.0"
minimal_mistakes_skin  : "dark"  # "air", "aqua", "contrast", "dark", "dirt", "neon", "mint", "plum", "sunrise"
```

Setup the repository properties in your site's `_config.yml`:
```yaml
respoitory: my-repo
```
To update the threme run `bundle update`.

Before running the site locally, you need to add `webrick` gem.
```bash
bundle add webrick
```

At this point you can run `bundle exec jekyll serve` to build the site and preview it in your browser at `http://localhost:4000`. You can also use the `--livereload` option to automatically rebuild the site when you make changes.
![](/assets/images/githubpages_setup/theme_setup.png)

## Step 3: Enable the profile sidebar
Enable the `author_profile` in your site's `index.markdown`:
```yaml
author_profile: true
```
Edit the `_config.yml` file to add your profile information:
```yaml
# Site Author
author:
  name             : "your name"
  avatar           : "/assets/images/your-avatar.png"
  bio              : "A brief description of your work."
  github           : "your-github-username"
  linkedin         : "linkedin-name" # (the last part of your profile url, e.g. https://www.linkedin.com/in/john-doe-12345678)
```
![](/assets/images/githubpages_setup/profile_setup.png)

## Step 4: Add a navigation bar
Create a new directory called `_data` in the root of your site. Then, create a new file called `navigation.yml` in the `_data` directory. Add the following contents to the `navigation.yml` file:
```yaml
main:
  - title: "Home"
    url: /
  - title: "About"
    url: /about/
  - title: "Contact"
    url: /contact/
```
![](/assets/images/githubpages_setup/navbar_setup.png)

## Step 5: Add content to the navigation bar sections
First of all, make sure to remove the `about.markdown` in your root directory.
Create a new directory called `_pages` in the root of your site. Then, create a new file called `about.md` in the `_pages` directory. Add the following contents to the `about.md` file:
```yaml
---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: splash
title: "About author"
permalink: /about/
date: 2022-10-01
---
<br>
What you want to add...
```

Update the `_config.yml` to load automatically the pages in the `_pages` directory:
```yaml
# Reading Files
include:
  - _pages
enconding: "utf-8"
markdown_ext: "markdown,mkdown,mkdn,mkd,md"
```

## Step 6: Adding posts
Inside the `_posts` directory, create a new file called `2022-10-01-first-post.md`. Add the following contents to the `2022-10-01-first-post.md` file:
```yaml
---
layout: single
title:  "My first post"
date:   2022-09-30 19:24:52 +0200
categories: githubpages posts
layout: single
---
This is my first post.

You can add lists:
* item 1
* item 2
```