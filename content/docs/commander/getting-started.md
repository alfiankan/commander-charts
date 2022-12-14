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

![get charts](/images/cmdr-get.gif)

## Using Commander


Then run `cmdr` the TUI will be shown. use `/` to open search. `arrow up` or `arrow down` to navigate through list. `enter` to select chart.

On the next screen you need to fill the blanks, some chart has default value so you left it blank to use default value. To Execute preformated command or snippet move your cursor by using `arrow up` or `arrow down` to hit `[Next]` button.

![base usage](/images/cmdr-base-usage.gif)


## Create local chart
Yess, you can create your own chart locally, you can do it manualy by copying chart foemat from `<your_home_directoy>/.commander` or using `cmdr mychart`

If you want to add or edit your own chart use `cmdr mychart -e <editor_choice>` you can specify text editor (code, vim, neovim, nano), or basicly yu can open your chart following name `mychart.chart.json` from `<your_home_directoy>/.commander`.

![base usage](/images/cmdr-create-chart.gif)


## Commander Codex
Commander codex bringing openai codex to your terminal, say good bay to context switching, ask right away on your terminal.
Before you can use commander codex you need to set openai token, if you dont have any yet please visit https://beta.openai.com/account/api-keys.


you can set openai token on your env, but is very recommended if you put the token in your bashprofile like  `.zshrc` using key value `OPENAI_API_KEY=myopenaitoken`

Commander codex is very easy to use just run `cmdr codex <your prompt>` for the example  `cmdr codex install zsh plugin auto suggestion`




