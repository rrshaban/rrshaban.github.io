---
layout: post
title:  "From zero to Hexo: a quick tutorial"
date:   2015-07-05 02:15:20
categories: 
---

[Hexo](https://github.com/hexojs/hexo) bills itself as a "A fast, simple & powerful blog framework", but I was blown away by how quickly I was able to get Hexo up and running. The main issue I had was finding the information I needed all in one place (this has [been](https://s1van.github.io/tags/tutorial/) [done](http://jdpaton.github.io/2012/11/05/setup-hexo/) [before](http://jr0cket.co.uk/2014/04/getting-started-with-hexo---a-modern-static-site-generator.html), with varying success). 

This tutorial will guide you through a fresh install to deploying a Hexo-powered blog to Heroku, with some discussion of the Hexo workflow I've settled into. The official tutorial is [here](https://hexo.io/docs/).



### Installing Hexo
Assuming you have node and npm installed, run `npm install -g hexo`. 

You should now be able to run `hexo init blog` to create a folder, `blog/`, with [a whole bunch of files](https://gist.github.com/rrshaban/e90d948a01323f022637), the vast majority of which are [the default theme](https://hexo.io/hexo-theme-landscape/). If you're curious about what these are, check out [the documentation](https://hexo.io/docs/setup.html). <!-- You can see from my footer that I use the [NexT theme](https://github.com/iissnan/hexo-theme-next), which I'll go over in a later section. -->



### Running Hexo locally

You can now run your `hexo server`, probably best in a [screen](https://github.com/rrshaban/screen_tutorial) or separate tab. 

{% highlight bash %}
INFO  Hexo is running at http://0.0.0.0:4000/. Press Ctrl+C to stop.
{% endhighlight %}

Open up [localhost:4000](http://localhost:4000/) to see a Hello World post with all the important Hexo commands:


> `$ hexo new "My New Post"`
> `$ hexo server`
> `$ hexo generate`
> `$ hexo deploy`



### Your first post


{% highlight bash %}
$ hexo new "My first post"
INFO  Created: blog/source/_posts/My-first-post.md
{% endhighlight %}


You can now edit that file in whatever text editor you prefer. Hexo creates a scaffolding for you to start with:


{% highlight bash %}

title: My first post
date: 2015-07-05 02:58:15
tags:
---
{% endhighlight %}


The local Hexo server will automatically detect any changes made to the file, so saving will be enough for you to preview your post on [localhost:4000](http://localhost:4000/).



### Generate static HTML

Running `hexo generate` will prompt Hexo to speedily render all of the static files necessary for the blog to `public/`. You can use Hexo as a tool to convert Markdown to HTML to run on a basic web server, though I prefer to host my site on Heroku.




### Deploying to Heroku

To install the Hexo Heroku deployer, run `npm install hexo-deployer-heroku --save`. Then add to your `_config.yml`:

{% highlight bash %}
deploy:
  type: heroku
  repo: git@heroku.com:<YOUR_HEROKU_NAME>.git
{% endhighlight %}

The default deploy message is `Site updated: {% raw %}{{ now('YYYY-MM-DD HH:mm:ss') }}{% endraw %}`, which works great for me. Now all you'll need to do to deploy your latest blog to Heroku is run `hexo deploy`. I've had some issues getting the deployer to recognize change made, so I advise running `generate` before you `deploy`. 

To install the Hexo Git deployer, run `npm install hexo-deployer-git --save`, and add the following to your `_config.yml`:

{% highlight text %}
deploy:
  type: git
  repo: <repository url>
  branch: [branch]
{% endhighlight %}



### My Hexo workflow

At this point, that's kind of it. The process is pretty straightforward:

1. `hexo new post`
2. Edit post.md in SublimeText
3. `hexo generate`
4. `hexo deploy`

And that's it! 


### Exploring further

If you're curious for where to start exploring more about Hexo, jr0cket has put together a [more involved workflow model](http://jr0cket.co.uk/developer-guides/hexo-workflow.pdf) and you can check out [the Hexo docs](https://hexo.io/docs/).

Another little thing I like: when you kill the server with a `^C`, Hexo responds with `INFO  Catch you later`. I love it.

Edit: A month after writing this post, I discovered another neat tidbit: `hexo list post`. Try it out!
