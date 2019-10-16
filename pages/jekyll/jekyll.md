---
layout: page
title: Jekyll
permalink: /jekyll
---

RubyInstaller
https://rubyinstaller.org/downloads/
Ruby+Devkit 2.5.3-1 (x64) 

It installs MSYS2. 
- MSYS2 base installation
- MSYS2 system update (optional)
- MSYS2 and MINGW development toolchain
   
Select all the 3 options one-by-one.
   
   
E:\mine\new>jekyll new kakagapo.github.io
Could not load Bundler. Bundle install skipped.
New jekyll site installed in E:/mine/new/kakagapo.github.io.


Execute the following command:
------------------------------
Based on info from the page https://github.com/jekyll/jekyll/issues/5165 did the following to setup bundler.
gem install bundler
bundle install

Now execute 
```
bundle exec jekyll serve
```

```
E:\mine\kakagapo.github.io>bundle exec jekyll serve
Configuration file: E:/mine/kakagapo.github.io/_config.yml
            Source: E:/mine/kakagapo.github.io
       Destination: E:/mine/kakagapo.github.io/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
       Jekyll Feed: Generating feed for posts
                    done in 1.301 seconds.
 Auto-regeneration: enabled for 'E:/mine/kakagapo.github.io'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
[2018-11-28 20:17:50] ERROR `/favicon.ico' not found.
```