---
layout:     post
title:      "Helpful Jekyll Resourses"
subtitle:   "Start your own blog and remedy some common gotchas."
date:       2015-07-31 09:00:00
author:     "Colin Rubbert"
header-img: "img/chem.png"
---

### Here are some fantastic resources for making your Jekyll game strong!

### Links:

[Jekyll Development Website](http://jekyllrb.com/)

[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

[Getting Your Jekyll Site on Github Pages](https://pages.github.com/)

[Other Sites Using Jekyll](https://github.com/jekyll/jekyll/wiki/Sites)

### Videos:

{% include youtubePlayer.html id="iWowJBRMtpc" %}

{% include youtubePlayer.html id="qJQNJcm-edk" %}

### Common Vagrant Gotchas:

+ Command not found: What is happening is that after the jekyll install the ability to execute `jekyll` needs to be initialized
  * To fix this you need to run `$ eval "(rbenv init -)"`

+ Can not access localhost: Vagrant is currently configured to forward port 3000 to 3030 and that's how we access our local server. The problem is that Jekyll runs by default on port 4000 which will not be accessible from our machine. You could go into the Vagrant configuration file and forward the port but that's just a hassle. Jekyll allows us to solve this issue two ways.
  * Instead of running the default Jekyll server command `$ jekyll serve` you will need to run `$ jekyll serve --host 0.0.0.0 --port 3000` and the problem is solved.
  * The other option is to go into the Jekyll `_config.yml` file and add `port: 3000` and `host: 0.0.0.0` underneath the `# Build Settings` section of the file.

+ Jekyll watch doesn't work properly in Vagrant. The command `jekyll serve --watch` or shorthand `jekyll serve -w` is designed to watch for changes and automatically apply those changes so you don't have to restart your server. The problem is that it doesn't work well with vagrant.
  * To solve you will want to run `jekyll serve -w --force_polling` this will force jekyll to pull the new changes.
