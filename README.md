
## Features

- [Live Search](https://github.com/thiagorossener/jekflix-template/wiki/Features#live-search)
- [Estimated Reading Time](https://github.com/thiagorossener/jekflix-template/wiki/Features#estimated-reading-time)
- [Reading Progress Bar](https://github.com/thiagorossener/jekflix-template/wiki/Features#reading-progress-bar) *(optional)*
- ["New Post" tag](https://github.com/thiagorossener/jekflix-template/wiki/Features#new-post-tag)
- [Load images on demand](https://github.com/thiagorossener/jekflix-template/wiki/Features#load-images-on-demand)
- [Push Menu](https://github.com/thiagorossener/jekflix-template/wiki/Features#push-menu)
- [SVG icons](https://github.com/thiagorossener/jekflix-template/wiki/Features#svg-icons)
- [Shell script to create posts](https://github.com/thiagorossener/jekflix-template/wiki/Features#shell-script-to-create-posts)
- [Tags page](https://github.com/thiagorossener/jekflix-template/wiki/Features#tags-page)
- [About page](https://github.com/thiagorossener/jekflix-template/wiki/Features#about-page)
- [Contact page](https://github.com/thiagorossener/jekflix-template/wiki/Features#contact-page)
- [404 error page](https://github.com/thiagorossener/jekflix-template/wiki/Features#404-error-page)
- [Feed RSS](https://github.com/thiagorossener/jekflix-template/wiki/Features#feed-rss)
- [Disqus](https://github.com/thiagorossener/jekflix-template/wiki/Features#disqus) *(optional)*
- [Featured post](https://github.com/thiagorossener/jekflix-template/wiki/Features#featured-post) *(optional)*
- [Home page pagination](https://github.com/thiagorossener/jekflix-template/wiki/Features#home-page-pagination) *(optional)*
- [Posts sidebar](https://github.com/thiagorossener/jekflix-template/wiki/Features#posts-sidebar) *(optional)*
- [Paginated posts](https://github.com/thiagorossener/jekflix-template/wiki/Features#paginated-posts) *(optional)*
- ["Before you go" modal](https://github.com/thiagorossener/jekflix-template/wiki/Features#before-you-go-modal) *(optional)*
- [Post recommendation](https://github.com/thiagorossener/jekflix-template/wiki/Features#post-recommendation)
- [Netlify CMS ready](https://github.com/thiagorossener/jekflix-template/wiki/Features#netlify-cms-ready)
- [Translations](https://github.com/thiagorossener/jekflix-template/wiki/setup#translations) **new!**
- [Math Expressions](https://github.com/thiagorossener/jekflix-template/wiki/Features#math-expressions) *(optional)* **new!**

## SEO

- Google Analytics
- Meta tags
- JSON-LD
- Sitemap.xml
- Social Media ready

## Quick Install

In the case you're installing to existing Jekyll project, add this line to your project's `Gemfile`:

```
gem "jekflix"
```

Add this line to your project's `_config.yml`:

```
theme: jekflix
```

And then run:

```
$ bundle
```

Or install it yourself as:

```
$ gem install jekflix
```

### Theme Colors

Create the file `/assets/css/styles.scss` and add:

```
---
---

$themeColor: #ff0a16;
$primaryDark: #141414;
$accentDark: #ffffff;
$lightGray: #f2f2f2;
$texts: #333333;

@import "jekflix";
```

Modify the variables above to change your theme colors.

### Site configuration

Below are some properties you can change in your project `_config.yml`, check the [documentation](https://github.com/thiagorossener/jekflix-template/wiki/settings) for more details.

```
# Site Settings
name: Jekflix
title: Jekflix | A blog theme for Jekyll
description: Jekflix is a template for Jekyll inspired by Netflix and made by Thiago Rossener.
tags:
  - blog
  - template
  - jekyll
  - theme
  - netlify
email: youremail@xyz.com
disqus_username: disqus_username
show_hero: true
menu:
  - title: Home
    url: /
  - title: About
    url: /about
  - title: Contact
    url: /contact
  - title: Feed
    url: /feed.xml

# Social Media Settings
# Remove the item if you don't need it
github_username: github_username
facebook_username: facebook_username
twitter_username: twitter_username
instagram_username: instagram_username
linkedin_username: linkedin_username
medium_username: medium_username

# Posts Settings
show_time_bar: true
show_modal_on_exit: false
show_modal_on_finish_post: true
two_columns_layout: true

# Advanced Settings
baseurl: "" # the subpath of your site, e.g. /blog
url: "" # the base hostname & protocol for your site
google_analytics: "UA-XXXXXXXX-X"
language: "en"
categories_folder: category
sent_message_url: "/contact/message-sent/"

# Build settings
markdown: kramdown
highlighter: rouge
permalink: /:title/
collections:
  authors:
    output: true
paginate_path: "/page/:num/"
show_get_theme_btn: true
use_logo: false

# Content paginator
paginate_content:
  enabled: true
  debug: false
  collections:
    - posts
  auto: false
  separator: "--page-break--"
  permalink: "/:num/"
  seo_canonical: true
  properties:
    part:
      is_generated: true
    last:
      is_generated: true
    single:
      is_generated: true

# SASS
sass:
  style: compressed

# Plugins
plugins:
  - jekyll-paginate
  - jekyll-paginate-content
```

## Setup

In the case you're cloning this repo, follow those instructions:

- [Environment](https://github.com/thiagorossener/jekflix-template/wiki/setup#environment)
- [Installing template](https://github.com/thiagorossener/jekflix-template/wiki/setup#installing-template)
- [Running local](https://github.com/thiagorossener/jekflix-template/wiki/setup#running-local)

### Customization

See the [settings documentation](https://github.com/thiagorossener/jekflix-template/wiki/settings) to customize layout, titles, social media and more.

### Theme

You can easily change the theme colors by changing the file `src/yml/theme.yml`, then running `gulp build` in your terminal.

#### GitHub pages

It's a known issue that you can't run Gulp when deploying the website into GitHub pages. So, you must change the theme colors and run `gulp build` locally, then push the changes into your repo, there is no other way.

To see how your website is going to look like when you deploy it, run `bundle exec jekyll serve` locally and access `http://127.0.0.1:4000/`.

## Posts

Use the [Front Matter properties](https://github.com/thiagorossener/jekflix-template/wiki/post#front-matter-properties) to create posts.

> **Note:** In the case you're cloning this repo, you can use the available [script](https://github.com/thiagorossener/jekflix-template/wiki/post#creating-a-post) to generate posts automatically.

## Release notes
