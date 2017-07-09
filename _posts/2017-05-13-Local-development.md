---
layout: post
comments: True
title: Local Development
---
After some trouble this seems to be partly working in local development mode.
What is not working is to put the content of the generated _site into a
a web server subdirectory. 
In _config.yml I have to put base.url: /
If I try base.url: /some_sub_directory links will be incorrect and the
theme decorations disappear.
Any suggestions for how to fix this?

---------------------------------------------------------------------------
I had to do:
* apt-get -y  install linux-headers-`uname -r`
* apt-get -y install make
* apt-get -y install ruby-dev
* apt-get -y install ruby-git
* apt-get -y install zlib1g-dev

* gem install bundler
* cd xgit
* bundle install
* and include in  _config.yml:
*  gems: [jekyll-paginate]

---------------------------------------------------------------------------
This recipe was not that simple!:
--------------------------------
Local Development

Install Jekyll and plug-ins in one fell swoop:
  gem install github-pages

This mirrors the plug-ins used by GitHub Pages
on your local machine including Jekyll, Sass, etc.

Clone down your fork:
  git clone https://github.com/yourusername/yourusername.github.io.git

Serve the site and watch for markup/sass changes:
  jekyll serve

View your website at http://127.0.0.1:4000/

Commit any changes and push everything to the master branch of your
GitHub user repository.
GitHub Pages will then rebuild and serve your website.
---------------------------------------------------------------------------







