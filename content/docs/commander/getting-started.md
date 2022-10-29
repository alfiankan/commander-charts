---
title: "Install commander"
weight: 2
description: >
  This page tells you how to get started with the Compose theme.
---


First ensure that your operating system meet requirements below.
- MacOS (amd64, x86_64, arm64)
- Linux (amd64, x86_64, arm64)

Install using script, copy then run on your terminal.

```bash
curl -sfL https://alfiankan.github.io/commander-charts/install.sh | sh -
```
or using Homebrew (brew).

```bash
brew tap alfiankan/homebrew-tap && brew install commander
```



To verify installation run.

```bash
cmdr -h
```

```bash
❯ cmdr -h
Commander TUI, create, run, share, prompt commands and snippets with ease

Usage:
  cmdr [flags]
  cmdr [command]

Available Commands:
  completion  Generate the autocompletion script for the specified shell
  get         get charts online
  help        Help about any command
  mychart     init or edit your own chart
  tojson      convert multiline text to json for snippet

Flags:
  -h, --help           help for cmdr
  -s, --shell string   set shell executor path (default "/bin/bash")

Use "cmdr [command] --help" for more information about a command.
```

## Download Commander Charts
Fisrt run `cmdr get --all` to download all available charts from official charts repo or just `cmdr get git` if you just need to download single chart by name on [Charts repo list](/charts)

-- gambar

## Using Commander


Then run `cmdr` the TUI will be shown.

-- gambar

- use `/` to open search.

-- gambar

- use `arrow up` or `arrow down` to navigate through list.

-- gambar

- use `enter` to select chart.

-- gambar

On the nect screen you need to fill the blanks, some chart has default value so you left it blank to use default value. To Execute preformated command or snippet move your cursor by using `arrow up` or `arrow down` to hit `[Next]` button.

-- gambar

## Create local chart
Yess, you can create your own chart locally, you can do it manualy by copying chart foemat from `<your_home_directoy>/.commander` or using `cmdr mychart`

-- gambar

If you want to add or edit your own chart use `cmdr mychart -e <editor_choice>` you can specify text editor (code, vim, neovim, nano), or basicly yu can open your chart following name `mychart.chart.json` from `<your_home_directoy>/.commander`.

-- gambar



