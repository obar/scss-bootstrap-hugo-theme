# SCSS Bootstrap

A vanilla [Bootstrap](https://getbootstrap.com/) theme for [Hugo](https://gohugo.io/). This is a fork of [a different theme](https://github.com/zwbetz-gh/vanilla-bootstrap-hugo-theme/), extending it to use Hugo Pipes for processing Bootstrap's Sass files for easier theme customization. The benefits include:

* Use variables to make global style changes in multiple places—things like [colors](https://getbootstrap.com/docs/4.4/getting-started/theming/#color) and [margins](https://getbootstrap.com/docs/4.4/getting-started/theming/#sass-options) can be consistent with a change in a single place
* Better organization of base styles and customization
* Automatically generate one minified css file for your whole site, with no additional dependencies
* Can include only css for functionality you are interested in—no need to import components you don't use in your site


## Table of Contents

* [Minimum Hugo version](#minimum-hugo-version)
* [Installation](#installation)
* [Updating](#updating)
* [Run example site](#run-example-site)
* [Configuration](#configuration)
* [Homepage content](#homepage-content)
* [Shortcodes](#shortcodes)
    * [bootstrap-blockquote](#bootstrap-blockquote)
    * [bootstrap-table](#bootstrap-table)
    * [bootstrap-card](#bootstrap-card)
* [Getting help](#getting-help)
* [Credits](#credits)

## Minimum Hugo version

The **extended** variant of Hugo version `0.60.1` or higher is required. View the [Hugo releases](https://github.com/gohugoio/hugo/releases) and download the binary for your OS. To ensure you have the extended version installed, you can run the following command and expect a non-empty return:

```
hugo version | grep extended
```

## Installation

From the root of your site:

```
git submodule add https://github.com/obar/scss-bootstrap-hugo-theme.git themes/scss-bootstrap-hugo-theme
```

## Updating

From the root of your site:

```
git submodule update --remote --merge
```

## Run example site

From the root of `themes/scss-bootstrap-hugo-theme/exampleSite`:

```
hugo server --themesDir ../..
```

## Configuration

Copy `config.yaml` from the [`exampleSite`](https://github.com/obar/scss-bootstrap-hugo-theme/tree/master/exampleSite), then edit as desired.

## Homepage content

By default the homepage uses the `homeText` param for content. If you wish to provide content from a file, then create `content/_index.md` and it will be used instead. For example:

```
---
title: Home
---

Homepage content goes here.
```

## Shortcodes

### blockquote

Uses [Bootstrap blockquotes](https://getbootstrap.com/docs/4.4/content/typography/#blockquotes) to format your blockquotes nicely. Pass the quote inside the shortcode. The `author` argument is optional.

[Here's an actual usage](https://raw.githubusercontent.com/obar/scss-bootstrap-hugo-theme/master/exampleSite/content/post/quotes-by-carl-jung.md), and here's an example usage:

```
{{< blockquote author="Carl Jung" >}}
Knowing your own darkness is the best method for dealing with the darknesses of other people.
{{< /blockquote >}}
```

### bootstrap-table

Uses [Bootstrap tables](https://getbootstrap.com/docs/4.4/content/tables/) to format your tables nicely. Pass the markdown table inside the shortcode, then pass the classes as an argument.

[Here's an actual usage](https://raw.githubusercontent.com/obar/scss-bootstrap-hugo-theme/master/exampleSite/content/post/style-a-markdown-table-with-bootstrap-classes-in-hugo.md), and here's an example usage:

```
{{< bootstrap-table "table table-dark table-striped table-bordered" >}}
| Animal  | Sounds |
|---------|--------|
| Cat     | Meow   |
| Dog     | Woof   |
| Cricket | Chirp  |
{{< /bootstrap-table >}}
```

### bootstrap-card

Uses [Bootstrap cards](https://getbootstrap.com/docs/4.4/components/card/) and [Hugo image processing](https://gohugo.io/content-management/image-processing/#readout) to display your [page bundle](https://gohugo.io/content-management/page-bundles/) images nicely. Only the `img`, `command`, and `options` arguments are required.

[Here's an actual usage](https://raw.githubusercontent.com/obar/scss-bootstrap-hugo-theme/master/exampleSite/content/post/nasa-images/index.md), and here's an example usage:

```
{{< bootstrap-card
img="sun.jpg"
command="Resize"
options="700x"
title="The Sun"
text="The Sun is the star at the center of the Solar System."
alt="sun"
class="mb-3"
style="" >}}
```

## Getting help

If you run into an issue that isn't answered by this documentation, then visit the [Hugo forum](https://discourse.gohugo.io/). The folks there are helpful and friendly. **Before** asking your question, be sure to read the [requesting help guidelines](https://discourse.gohugo.io/t/requesting-help/9132).

## Credits

In addition to Bootstrap and Hugo, thank you to:

* [Feather](https://feathericons.com/) for icons
* [zwbetz-gh](https://github.com/zwbetz-gh/vanilla-bootstrap-hugo-theme/) for creating the initial theme
