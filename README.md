# vmous.github.io

My GitHub.io pages: https://vmous.github.io/

The pages use [Jekyll](https://jekyllrb.com/) based on the [Indigo Minimalist Template](https://github.com/sergiokopplin/indigo)

## Setup

Clone the repositry

``` shell
$ git clonehttps://github.com/vmous/vmous.github.io.git
```

Add a remote to the inigo repository

``` shell
$ git git remote add upstream https://github.com/sergiokopplin/indigo.git
$ git remote -vv
origin  https://github.com/vmous/vmous.github.io.git (fetch)
origin  https://github.com/vmous/vmous.github.io.git (push)
upstream        https://github.com/sergiokopplin/indigo (fetch)
upstream        https://github.com/sergiokopplin/indigo (push)
```

You’ll need to have [Ruby](https://www.ruby-lang.org/en/) and [Bundler](https://bundler.io/) installed. Setup [rbenv](https://github.com/rbenv/rbenv) in order to easily manage your Ruby configuration per-project.

Install Ruby 2.4.0+ according to Jekyll's requirements:

``` shell
$ rbenv install 2.7.0
```
In the project's root directory set to use the Ruby you just installed:

``` shell
$ rbenv local 2.7.0
```

Double check you are using the correct Ruby version managed by rbenv

``` shell
$ rbenv versions
  system
* 2.7.0 (set by /Users/vmous/Workspace/vmous.github.io/.ruby-version)
$ ruby -v
ruby 2.7.0p0 (2019-12-25 revision 647ee6f091) [x86_64-darwin18]
```

Make sure you have Jekyll and [Bundler](https://bundler.io/) installed

``` shell
$ gem install jekyll bundler
```

Build the static website

``` shell
$ bundle install
```

Start the local server

``` shell
$ bundle exec jekyll serve --config _config.yml,_config-dev.yml --watch --port 4444
```

Use your browser to open http://localhost:4444


## Merge latest

Get the latest of your upstream

``` shell
$ git fetch upstream
```

Get the latest tags from your upstream

``` shell
$ git ls-remote --tags upstream
```

Locate the latest tag in the above commands output. On the left it should show the tag's SHA-1 hash. Make sure this hash is the same as in the hash in the tags directory

``` shell
$ cat ./.git/refs/tags/1.0.1
```

If not retry fetching the tags

``` shell
$ git fetch --all --tags
```

Checkout the tag in a branch

``` shell
$ git checkout tags/1.0.1 -b 1.0.1-branch
```

Pick the latest and check it out in a local branch

``` shell
$ git 
```
