# JSDayES Blog

[![Build Status](https://travis-ci.org/jsDayES/blog.svg?branch=master)](https://travis-ci.org/jsDayES/blog)

Blog for JSDayES.

#### Requirements:

- [nvm](http://github.com/creationix/nvm)
- [hexo](http://hexo.io/)
- git
- A text editor


### Setup

```
nvm install 9.8.0
nvm use
npm install
```


### Commands

- `hexo clean`     Remove generated files and cache.
- `hexo deploy`    Deploy your website.
- `hexo generate`  Generate static files.
- `hexo help`      Get help on a command.
- `hexo list`      List the information of the site
- `hexo new`       Create a new post.
- `hexo publish`   Moves a draft post from _drafts to _posts folder.
- `hexo server`    Start the server.


### Deploy (to gh pages)

```
hexo clean && hexo generate && hexo deploy
```
