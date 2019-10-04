---
layout: post
title:  "How to install jekyll on Debian 10 Buster as user"
---

### Install requirements to install rubygems
`sudo aptitude install ruby-dev rubygems`

### Install jekyll and bundler as user
`gem install jekyll bundler --user-install`

### Add gem binaries to PATH
`vim ~/.bashrc` and add, e.g.,
```bash
if [ -d "$HOME/.gem/ruby/2.5.0/bin" ]; then
    export PATH="$PATH:$HOME/.gem/ruby/2.5.0/bin"
    export GEM_HOME="$HOME/.gem/ruby/2.5.0"
fi
```
Make the change active in current bash
`source ~/.bashrc`
