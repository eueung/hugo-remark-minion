# hugo-remark-minion
Manage and write remark.js slides with Hugo.

I'm using [remark](https://github.com/gnab/remark) quite a lot for my slides and weirdly also for documentation. It helped a lot, especially if you have a bunch of **codes** to be displayed. Previously I'm using some scripts to manage content before it passed to remark for final rendering. This project is an attempt (and an experiment) to manage content entirely with Hugo. What does it have to do with minions? :-) .. just look at the demo below! Don't worry, jackie is also there.

![Screenshot](https://raw.githubusercontent.com/eueung/hugo-remark-minion/master/images/screenshot.png)

## Demo

- [Official Remark Slides + Minions](//eueung.github.io/hugo-remark-minion/)

## Installation

Inside the folder of your Hugo site run:

    $ cd themes
    $ git clone https://github.com/eueung/hugo-remark-minion.git remark-minion

For more information read the official [setup guide](//gohugo.io/overview/installing/) of Hugo.

## Sample Configuration

The following `config.toml` is used for the demo site mentioned above.

```toml
baseurl         = "/"
theme           = "remark-minion"
languageCode    = "en-us"
title           = "Site Title | Hugo Remark-Minion"
canonifyurls    = true

[params]
  googleAnalytics = ""
  name            = "Eueung Mulyana"
  description     = "Demo slides for Hugo Remark Minion"
  custom_css      = ["custom.css"]
```

## Sample Content

Sample content structure is given in the `exampleSite` folder. Because of the current (v0.18) implementation of `.RawContent` which does not render Hugo shortcode, page variable `contentType` must be set to `sc` (abbreviated shortcode), otherwise it has to be set to `md` (markdown). The above screenshot was produced with the following source.

```
+++
contentType = "sc"
weight = 6
+++

{{< minion_waaat_right title="#Waaat" >}}
Schon Wieder Untericht?
.blue[No.no.no]!
{{< /minion_waaat_right >}}
```
## Sample Style

Usually you'll maintain your own custom CSS. This has to be declared in the `config.toml`. Sample style is included in the `exampleSite/static/css` folder.

Have fun!

## License

This theme is released under the MIT license. For more information read the [License](//github.com/eueung/hugo-remark-minion/blob/master/LICENSE.md).

