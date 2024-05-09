# Horse theme for Hugo

The theme for my blog. 
Forked from [Rocinante](https://github.com/mavidser/hugo-rocinante)

## Features

...

## Installation

Inside the folder of your Hugo site run:

    $ git submodule add https://github.com/coleww/horse.git themes/horse

For more information read the official [setup guide](//gohugo.io/overview/installing/) of Hugo.

## Configuration options

Put these in the `params` section of config.toml

- **customCSS** - An array of paths to css files in the `assets` directory. Eg: `customCSS = ["css/style.css"]`.
- **mainSections** - An array containing tags that should be displayed on the homepage
- **favicon** - A string of the favicon path in the `static` directory.  Eg: `favicon = "icon/favicon.jpg"`
- **about** - A string of the about text. This is slightly ugly, sorry. Eg: `about = """Hi. Welcome to my website"""`
- **links** - A table which contains array of `link` tables. This one is easier to explain using an example. Details of the link `table`:
  - name - String containing the text of the link
  - href - String containing URL of the link
  - new_tab = Boolean, to open link in a new tab
  
  Example:
  ```toml
  [[params.links]]
    [[params.links.link]]
      name = "About"
      href = "https://en.wikipedia.org/wiki/Don_Quixote"
      new_tab = true
  ```
- **projects** - A table which contains array of `project` tables. Has same format as `links`. 
  ```

## Getting started

After installing the theme successfully it requires a just a few more steps to get your site running.

### Update config file

Example:

```toml
baseURL = "https://example.com/"
languageCode = "en-us"
title = "My Blog"
theme = "horse"
paginate = 3

[markup]
  [markup.highlight]
    style = "monokailight"
  [markup.goldmark.renderer]
    unsafe= true

[params]
  mainSections = ["tech", "outdoors"]
  favicon = "icons/favicon.png"
  about = """
About section. Enter details about you here.
"""

  [[params.links]]
    [[params.links.link]]
      name = "Resume"
      href = "/Resume.pdf"
    [[params.links.link]]
      name = "Email"
      href = "/contact"
      smart_email_link = true

  [[params.projects]]
    [[params.projects.project]]
      name = "My cool app"
      href = "https://github.com/"
      new_tab = true
    [[params.projects.project]]
      name = "A thing I did"
      href = "https://mastodon.social/"
      new_tab = true
```

### Check your site

In order to see your site in action, run Hugo's built-in local server.

`$ hugo server`

Now enter [`localhost:1313`](http://localhost:1313/) in the address bar of your browser.

## License

MIT
