# JSDayEs Theme

__jsdayes is a simple blog theme focused on writing. In such a trend of complex typography, choose the return to origins, focusing on writing this matter.__

The beginning is [moyo](http://liuxinyu.me/) created a theme of Wordpress , by DaraW transplanted to Hexo as [Hacker](https://github.com/CodeDaraW/Hacker) theme by [CodeDaraW](https://github.com/CodeDaraW)).


## Installation

Apply the theme in the hexo global configuration file `_config.yml`:

```yaml
theme: jsdayes
```
Now all are in order, just enjoy~

__Notice: After every update, you'd better run command `hexo clean` to clean cache files before Hexo generating, in case of some problems cache files bring.__


## Configure
### Enable comments and Google Analytics
In the theme configuration file `_config.yml`:

```yaml
# duoshuo comment
duoshuo: true
duoshuo_name:

# disqus comment
disqus: false
disqus_shortname:

# google analytics
googleTrackId:
```


`duoshuo`: `boolean`, use duoshuo or not;
`duoshuo_name`: `string`, your duoshup ID, please don't use other people's IDs。

`disqus`: `boolean`, use disqus or not;
`disqus_shortname`: your disqus site shortname.

`googleTrackId`: your Google Analytics ID, jsdayes will not use Google Analytics if it's empty.

### Enable Categories and Tags pages
Categories Page: run `hexo new page categories`，then modify the generated file `source/categories/index.md`：
``` markdown
title: categories
date: 2017-01-30 19:16:17
layout: "categories"
---
```
If you need to close comments of this page , you can add a line `comments: false`; `title` corresponds to the title of the page.

Tags Page: run `hexo new page tags`，then modify the generated file `source/tags/index.md`：
``` markdown
title: tags
date: 2017-01-30 19:16:17
layout: "tags"
---
```
Configuration is the same as Categories Page.

Add links to the menu: Edit the `_config.yml` file of the theme, add `Categories: /categories` and `Tags: /tags` in `menu` like this：
``` yml
menu:
  Home: /
  Archives: /archives
  Categories: /categories
  Tags: /tags
```

## License
GNU GPL(General Public License) v2.0
