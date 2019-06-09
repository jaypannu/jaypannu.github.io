---
layout: post
title:  Jekyll github-pages setup"
date:   2019-06-09 01:25:21 +0530
categories: python terminal ubuntu
---

Maybe better to follow github guide on setting github pages with jekyll. It may change in future. 

Install ruby - snap is latest as compared to apt but may not be safe

```
sudo snap install ruby --classic
```

Install the bundler gem

```
gem install bundler
```

Create a gem file with following code
```
source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins
```

Run following to install all depenedecies as per Gemfile:
```
bundle install
```

This is failing on ubuntu 19.04, as of Jun 20189. As per solution pasted here:


https://github.com/eventmachine/eventmachine/issues/881


We try to install ruby with RVM (ruby version manager)

First instll gnupg2 and curl
```
sudo apt install gnupg2
sudo apt install curl
```

Get key from here: https://rvm.io/

Install ruby + rails, feels like overkill to just build one static site (?)

```
gpg2 --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
\curl -sSL https://get.rvm.io | bash -s stable --rails
```

To use ruby add following:
```
source /home/luffy/.rvm/scripts/rvm
```

Create a new site:
```
bundle exec jekyll _3.3.0_ new web
```

In Gemfile change following: comment gem jekyll line and uncomment github line

To run the site locally:
```
bundle exec jekyll serve
```
