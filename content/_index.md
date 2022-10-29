+++
title = "Commander TUI"
[data]
baseChartOn = 3
colors = ["#627c62", "#11819b", "#ef7f1a", "#4e1154"]
columnTitles = ["Section", "Status", "Author"]
title = "Projects"

+++
{{< block "grid-2" >}}
{{< column >}}

# Create, run, share command and snippet with **Ease**.


> Install now preview available for Linux (arm64, amd64) and MacOS (arm64, amd64) by running the script below
```bash
curl -sfL https://alfiankan.github.io/commander-charts/install.sh | sh -
```

or using Homebrew (brew).

```bash
brew tap alfiankan/homebrew-tap && brew install commander
```

{{< tip "warning" >}}
Feel free to open a [Pull request](https://github.com/alfiankan/commander/pulls), or contribute to create new chart on [Commander Charts](https://github.com/alfiankan/commander-charts/pulls). {{< /tip >}}

{{< tip >}}
v0.1.0
- charts explorer, find, prompt and execute command
- charts manager, download charts from online main charts repository
- charts manager, override repo using self hosted charts repository
- charts manager, create owned chart locally
- chart manager, code editor integration (vscode, vim, neovim, nano)

{{< /tip >}}

{{< tip "warning" >}}
Planned v0.2.0
- prompter, terminal like path autocomplete
- prompter, multi choice prompter

{{< /tip >}}



{{< button "docs/" "Read the Docs" >}}
{{< button "charts/" "Charts Table" >}}{{< /column >}}


{{< column >}}
![diy](/images/scribble.jpg)
{{< /column >}}
{{< /block >}}
