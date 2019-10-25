---
layout: page
title: Jekyll
permalink: /jekyll
---

### Important commands:
- To setup new site
```$ jekyll new jekyll_site``` 
- To install dependencies
```bundle install```
- To update dependencies
```bundle update```
- To serve the site at 127.0.0.1:4000
```bundle exec jekyll serve```

jekyll serve output
------------------------------
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

### Alternate themes:
- [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/) : source can be found [here](https://github.com/mmistakes/made-mistakes-jekyll/tree/master/src)

### Note: 
- Changes to ```_config.yml``` requires restarting jekyll
- Use [collections](https://jekyllrb.com/docs/collections/) to organize the data. Before the introduction of the ```cs``` collection to this site the top navigation had links to all the pages in the site (because that is what minima theme does).
- If  ```bundle exec jekyll serve``` fails with messsage saying ```can't find gem bundler``` when you know for sure bundler is installed, it might be because the bundler version in the Gemfile.lock does not match the version installed. This was a problem with older versions of gem and updating gem will fix the issue.

```
$ bundle exec jekyll serve
Traceback (most recent call last):
	2: from /home/kakagapo/gems/bin/bundle:23:in `<main>'
	1: from /usr/lib/ruby/2.5.0/rubygems.rb:308:in `activate_bin_path'
/usr/lib/ruby/2.5.0/rubygems.rb:289:in `find_spec_for_exe': can't find gem bundler (>= 0.a) with executable bundle (Gem::GemNotFoundException)
```
```
$ sudo gem update --system
[sudo] password for kakagapo: 
Updating rubygems-update
Fetching: rubygems-update-3.0.6.gem (100%)
Successfully installed rubygems-update-3.0.6
Parsing documentation for rubygems-update-3.0.6
Installing ri documentation for rubygems-update-3.0.6
Installing darkfish documentation for rubygems-update-3.0.6
Done installing documentation for rubygems-update after 49 seconds
Parsing documentation for rubygems-update-3.0.6
Done installing documentation for rubygems-update after 0 seconds
Installing RubyGems 3.0.6

...

RubyGems system software updated
```

- Still having issues ? Try running ```bundle install``` to get the missing gems.

```
$ bundle exec jekyll serve
Could not find public_suffix-4.0.1 in any of the sources
Run `bundle install` to install missing gems.
$ bundle install
Fetching gem metadata from https://rubygems.org/...........
Fetching gem metadata from https://rubygems.org/.
Resolving dependencies...
Fetching public_suffix 4.0.1
...
Installing minima 2.5.1
Bundle complete! 4 Gemfile dependencies, 28 gems now installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.
```