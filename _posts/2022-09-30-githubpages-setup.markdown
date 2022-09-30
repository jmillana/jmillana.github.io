---
layout: single
title:  "Setting up GitHub Pages from scratch"
date:   2022-09-30 19:24:52 +0200
categories: jekyll update
---
This post is a step-by-step guide on how to set up a GitHub Pages site from scratch. It is based on the [official documentation](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll) and the [Jekyll docs](https://jekyllrb.com/docs/).
For the sake of simplicity, I will assume that you have a GitHub account and that you have already created a new repository for your site. If you haven't done so, you can follow the [official documentation](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll) to create a new repository.
For the sake of simplicity, I will also assume that you have a local installation of Ruby and RubyGems. If you don't, you can follow the [official documentation](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll) to install Ruby and RubyGems.
Finally, I will assume that you have a local installation of Jekyll. If you don't, you can follow the [official documentation](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll) to install Jekyll.
## Step 1: Create a new Jekyll site

To create a new Jekyll site, you can use the `jekyll new` command. This command will create a new Jekyll site in the current directory. If you want to create a new Jekyll site in a different directory, you can use the `--path` option. For example, if you want to create a new Jekyll site in a directory called `my-site`, you can use the following command:

```bash

jekyll new --path my-site

```

## Step 2: Add a theme (minimal-mistakes)