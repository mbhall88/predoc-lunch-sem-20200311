<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [EBI reveal-hugo template](#ebi-reveal-hugo-template)
- [Install](#install)
- [Usage](#usage)
  - [Serve](#serve)
  - [Edit](#edit)
  - [Theme/Styling](#themestyling)
  - [Logo](#logo)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# EBI reveal-hugo template

This repository is a template for a minimal EMBL-EBI-themed [reveal.js][revealjs] presentation.  

# Install

Firstly, to develop the presentation, you need to have [Hugo][hugo] installed.

```sh
brew install hugo
# also install optional Pygments package for syntax highlighting in presentation
pip3 install Pygments
```

Hugo will serve the presentation as a local static site in your web browser and update as
you make changes in the source code of the presentation.

Next, clone this template in a directory (ideally named for your presentation)

```sh
presentation="awesome_conference"
git clone https://github.com/mbhall88/reveal-hugo-ebi "$presentation"
cd "$presentation"
git submodule update --init
```

# Usage

## Serve

To serve the presentation in your web browser run the following from the root directory
of the repository.

```sh
hugo serve
```

In your web browser, navigate to http://localhost:1313/ . Every time you make changes
this webpage will auto-reload to reflect those changes.

You should see a screen that looks like this

![Template screenshot](static/images/screenshot.png?raw=true)


## Edit

The [reveal-hugo docs][reveal-hugo] have a great [tutorial][reveal-hugo-tut] to get you
up and running. There is also a thorough blog post [here][forestry-blog].

The `config.toml` is a central place for defining the settings of your presentation.
A full list of configurations can be found [here][config].

The slides themselves are within `content/`. `_index.md` is the "root" for your slides
and you can also define presentation-wide settings in this file too. You can put all of
your slides in `_index.md` if you wish, but you can likewise break them up into sections.
Sections will be vertically stacked within the presentation when placed in `content/home/`.

So if we had an `_index.md` file that looked like This

```md
+++
title = "My presentation"
outputs = ["Reveal"]
+++

# Hello, world!

This is my first slide.

---

# Hello Mars!

This is my second slide

---

## Mars method

This slide describes the methods and has a pretty plot
```

We could move the slides about Mars into their own section with the following setup.

`content/_index.md`
```md
+++
title = "My presentation"
outputs = ["Reveal"]
+++

# Hello world!

This is my first slide.
```

`content/home/mars.md`
```md
+++
weight = 10
+++
{{% section %}}
# Hello Mars!

This is my second slide

---

## Mars method

This slide describes the methods and has a pretty plot.
{{% /section %}}
```

*Note: `weight` is how you define the order of slides. If you have another `.md` file
with `weight = 11` it will come after `content/home/method.md`. See [this][weight] for more info.*

For more information on sections, see [the docs][sections].


## Theme/Styling

If you would like to make any changes to the font, colours, style etc. then this can be
done in `static/stylesheets/robot-lung-ebi.css`. The current stylesheet is a copy of
the [robot-lung][robot-lung] theme, which I have changed some colours to match the EBI
colour scheme.

## Logo

There are two forms of the EBI logo, which can be found in `static/logos/`. There is one
for white background presentations (`ebi_white_bg.svg`) and one for dark backgrounds
(`ebi_dark_bg.svg`).  
If you would like to make any changes to the size, layout, or which logo is used, then
instructions can be found in [this short tutorial][reveal-hugo-logo].






[revealjs]: https://revealjs.com/
[hugo]: https://gohugo.io/
[reveal-hugo-tut]: https://github.com/dzello/reveal-hugo#tutorial
[reveal-hugo]: https://github.com/dzello/reveal-hugo
[forestry-blog]: https://forestry.io/blog/harness-the-power-of-static-to-create-presentations/
[config]: https://github.com/dzello/reveal-hugo#configuration
[weight]: https://forestry.io/blog/harness-the-power-of-static-to-create-presentations/#additional-markdown-files
[robot-lung]: https://revealjs-themes.dzello.com/robot-lung.html#/
[reveal-hugo-logo]: https://reveal-hugo.dzello.com/logo-example/#/
[sections]: https://github.com/dzello/reveal-hugo#root-vs-section-presentations
