<p align="center">
    <img width="500" src="assets/cover.png" />
</p>

👋 Hello! This is an RSS reader which allows you to browse the web better! It's accompanied by a beautiful TUI made
with [bubble tea](https://github.com/charmbracelet/bubbletea)

## ❤️ Getting started

Installing is extremely easy with `go install`

```
go install github.com/TypicalAM/goread/cmd/goread@latest
```

Which produces a `goread` executable

## 📸 Here is a demo of what it looks like:

Here is some basic usage:

<p align="center">
    <img width="700" src="assets/example1.gif" />
</p>

Here we use `pywal` to generate a colorscheme from an image and then convert it to a goread colorscheme!

<p align="center">
    <img width="700" src="assets/example2.gif" />
</p>

## ⚙️ Configuration

### 📝 The urls file

The urls file contains the categories and feeds that you are subscribed to! This file is generated by the program at
the `~/.config/goread/urls.yml` location and looks similar to this:

```yaml
categories:
  - name: News
    desc: News from around the world
    subscriptions:
      - name: BBC
        desc: News from the BBC
        url: http://feeds.bbci.co.uk/news/rss.xml
  - name: Tech
    desc: Tech news
    subscriptions:
      - name: Wired
        desc: News from the wired team
        url: https://www.wired.com/feed/rss
      - name: Chris Titus Tech (virtualization)
        desc: Chris Titus Tech on virtualization
        url: https://christitus.com/categories/virtualization/index.xml
```

You can edit this file yourself or create a script which can for example automatically add a feed from your clipboard!

### 🌃 The colorscheme file

The colorscheme file contains the colorscheme of your application! It can be generated by hand or using
the `--get_colors` flag. The colorscheme file is put by default in `~/.config/goread/colorscheme.json` - an example file
would look something like this!

```json
{
  "BgDark": "#040612",
  "BgDarker": "#040612",
  "Text": "#98ccdc",
  "TextDark": "#98ccdc",
  "Color1": "#625160",
  "Color2": "#BD4354",
  "Color3": "#985063",
  "Color4": "#BA9C6A",
  "Color5": "#1E5AA6",
  "Color6": "#C25C9F",
  "Color7": "#98ccdc"
}
```

If you use the `--get_colors` flag to generate a colorscheme from pywal you have to supply it with the
pywal `colors.json` file which is usually located at `~/.cache/wal/colors.json`.

## ✨ Tasks to do

Here are the things that I've not yet implemented, contributions and suggestions are very welcome!

- [X] A main category where all the feeds are aggregated
- [X] Moving the help to the bubbletea `help` bubble

## 💁 Credit where credit is due

### Libraries

The demo was made using [vhs](https://github.com/charmbracelet/vhs/), which is an amazing tool, and you should
definitely check it out. The entirety of [charm.sh](https://charm.sh) libraries was essential to the development of this
project. The [cobra](https://github.com/spf13/cobra/) library helped to make the cli flags and settings.

### Fonts & logo

The font in use for the logo is sen-regular designed by "Philatype" and licensed under Open Font License. The icon was
designed by throwaway icons.

