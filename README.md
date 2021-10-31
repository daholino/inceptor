# Inceptor - Hugo theme

Inceptor is a simple, fast and responsive Hugo theme for blogging.

>I wanted to start blogging and I couldn't find the theme that fit my needs so I decided to create *Inceptor*. I am still new in the world of Hugo so I will address all the issues and add more improvements as I learn.

You can find the demo [here](https://tarikdahic.com).

## Screenshots

<p float="left" align="middle">
<img src="/docs/screenshots/ss-home.png?raw=true" width="200" height="200">
<img src="/docs/screenshots/ss-markdown.png?raw=true" width="200" height="200">
</p>

## Features

- Minimal and fast
- SEO friendly
- Disqus support
- Google Analytics support
- Customizable
- Dynamic social networks (links) on homepage
- Cover images on posts

## Installation

Clone this repo and add it to themes folder of your Hugo site. Configure the theme via *config.toml* of your site and add appropriate images if needed to your static folder. Check out the example config below to see what can you customize.

 ### Config

 This is the config that I use for my site. It uses all available options for customization and it can be a really great starting point for you:

 ```toml
baseURL = 'https://tarikdahic.com/'
languageCode = 'en-us'
title = '<your-site-name>'
theme = 'inceptor'
pygmentsUseClasses = true
pygmentsCodefences = true
paginate = 20
disqusShortname = '<your-disqus-shortname>'
googleAnalytics = '<your-google-analytics-tracking-id>'

[params]
indexMessage = 'Tarik Dahic'
indexDecription = 'Software Engineer. Passionate about creating products.'
indexAdditional = 'Currently iOS Developer at Bicom Systems.'
icon = '/icon.svg'
personalImage = '/personal.png'
footerMessage = 'Copyright © 2021 Tarik Dahic'
images = ['images/share.png']

[[params.socials]]
  icon = 'twitter'
  link = 'https://twitter.com/daholino'

[[params.socials]]
  icon = 'linkedin'
  link = 'https://www.linkedin.com/in/tarikdahic/'

[[params.socials]]
  icon = 'github'
  link = 'https://github.com/daholino'

[markup.highlight]
guessSyntax = true
lineNoStart = 1
lineNos = false
noClasses = false

[menu]
  [[menu.main]]
    name = "Home"
    url = "/"
  [[menu.main]]
    name = "Posts"
    url = "/posts/"
  [[menu.main]]
    name = "Tags"
    url = "/tags/"
 ```

### Archetypes

The theme ships with one `default.md` archetype. This is the contents of it:

```yaml
---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
tags: [] # add tags here like ["tag", "another-tag"]
images: [] # the first image will be used for opengraph and twitter meta tags
featured_image: "" # this image will be displayed as a thumbnail on post list and as a cover on post page
summary: "" # summary that will be displayed on posts lists
---
```

You can use `hugo new posts/post-name.md` to generate a new post using these options but make sure that you don't override this archetype by the one from the root hugo folder.

## Roadmap

I plan to add more features to this theme. Some of them are:

- Dark mode
- Image preview
- Improved syntax highlighting
- Related posts suggestions

If you have any requests or ideas please do not hesitate to open an issue in the project so that we can discuss it and implement it!

## Development

Want to contribute? Great! I'll take all the help that I can get.

Inceptor is not using any dependency managers like npm or webpack for bundling. To start developing just clone the theme and tweak the code :)

## Dependencies

Inceptor uses following scripts, plugins and projects:

- [instant.page](https://instant.page)
- [feather](https://github.com/feathericons/feather)
