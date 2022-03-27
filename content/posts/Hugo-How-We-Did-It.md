---
title: Web Development With Hugo. 
date: 2022-03-26
description: 'Hugo is a static site generator. It is how we built this beauty of a site. We also gotta thank JugglerX for the theme itself.'

---

# Hugo. What is it?

## Hugo is a static site generator and is a great way to make websites.

**However, it really should not be on this website, because it takes way longer than 30 minutes, but we made this website with it so I thought it would be nice to document our methods.**

These videos more or less encapsulate the general tasks of setting up hugo. I used them and they were a pillar to lean on.

[RWaltr’s video](https://www.youtube.com/watch?v=-q6ZiCroiGM&ab_channel=Rwaltr)
[Giraffe Academy](https://youtu.be/G7umPCU-8xc)

From that I have a few tips. For the exampledomain use nothing or a /. It creates the links between pages fine with that. 

Second, use the example site. Almost all the templates you will find on the hugo site will have a great example site within the themes folder. It will allow you to copy and paste it into your root folder for hugo and just edit it like any other template.

The benefits of Hugo are that it is fast. Really fast. It also is easy for collaboration with non developer friends because markdown can be learned by anyone in 5 minutes. It is also easy for me, the non-developer, to work out. Hugo’s syntax error codes are really specific.

Onto the specifics of our website. We are hosting off of github pages. I used github for the first time and cloned the theme repo we were using to my theme folder that Hugo made for me: [Hugo-Winston](https://hugo-winston.netlify.app/). Then I copied the example site that the theme has and took its assets and replaced the default empty ones in the root directory of the site /hugo/hoohacks. I am not explaining this well, so this is not a guide, watch the videos if you need one. This is to iterate, just to tell you what we did. From that we just edited the example content, config.toml file, data files to our liking. It was pretty self-explanatory. Change the data within the quotations to be what you want.
Our first hiccup was embedded youtube videos. Our solution was fast. We created an archetype, which I don’t entirely understand, that allows us to run RAW html allowing embedded code to work. The two tips I listed earlier were also problems I had. Using Hugo without anyone really helping me, and without many windows related tutorials was challenging. I’m glad I understand basic HTML and CSS because it helped so much when determining issues. There is so much I could write about Hugo, but it doesn’t matter. Go and do it yourself. Our website will be available on github for you to see. I will also post my files for the website before Hugo spits it out as static assets. A sort of second example for you.

**Thanks for reading**. It means the world.

This is my config.toml file. The fun part about hugo is trying to figure out what changes in the config do.

```
baseURL = "/"
languageCode = "en-us"
title = "1period"
themesDir = "themes"
theme = "hugo-winston-theme"

pygmentsCodeFences = true
pygmentsCodefencesGuessSyntax = true
pygmentsUseClasses = true
paginate = 3

[module]
  [module.hugoVersion]
    extended = true
    min = "0.55.0"

[params]
  google_analytics_id = ""
  twitter_handle = "@zerostaticio"

  showAuthorOnHomepage = true
  showAuthorOnPosts = true
  showPostsOnHomepage = true

  addFrame = true
  addDot = true

  highlightColor = '#3399ff'
```
