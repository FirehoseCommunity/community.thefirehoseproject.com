# Firehose Community

Here lies the official [Firehose Community](http://community.thefirehoseproject.com) blog.

Technical talks and coding related topics will be here!

## How to Contribute Articles to the Firehose Community

1. Fork the site
2. Get the blog running on your system
3. Write a post
4. Add your article on your GitHub page
5. Issue a [Pull Request](https://github.com/FirehoseCommunity/community.thefirehoseproject.com/compare) for your blog post.

## Getting the blog up and running

This blog is using Jekyll one of the most popular static site generation tools.  To understand the broad strokes of Jekyll watch [Colin's Talk on Jekyll](http://community.thefirehoseproject.com/2015/07/16/colin-rubbert-talks-about-jekyll.html).

### Installation on a Vagrant Ubuntu Machine

**Install Jekyll**

Install the Jekyll Gem

```
gem install jekyll
```

Then update the binary (if you don't do this it will say command-not-found if you run `jeckyll` command):

```
rbenv rehash
```

**Install Grunt**

This uses a theme in Jekyll that requires `Grunt` which is an asset manager (kind of like the asset pipeline in rails, without rails).

Grunt requires a bunch of steps to install it.

You might have an old version of Node on your environment.  Run this command to remove it all together:

```
sudo apt-get remove node nodejs
```

Then installthe right `Node` on the machine:

```
sudo add-apt-repository ppa:chris-lea/node.js
sudo apt-get update
sudo apt-get install nodejs -y 

```

Then update `NPM`: 

```
npm update
```

Then install `Grunt`:

```
npm install grunt
```

### Running the blog

Clone your fork and in the directory run the command to start the server:

```
jekyll serve --host 0.0.0.0 --port 3000
```

The first time you run this command it will take a while to get loaded up.



This is based off [this](https://github.com/IronSummitMedia/startbootstrap-clean-blog-jekyll) theme.


# Contributors

Get your name on this list of firehosers!

* Colin Rubbert
* Angel Jose
* Ben Ricker
* Ilya Krasnov
* Ken Mazaika