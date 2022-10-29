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


<h1 style="background-color:green;max-width: fit-content;padding:2px;padding-right:10px; padding-left:10px;" id="anima"></h1>
<h1>command and snippet with <b>Ease</b></h1>

<script>
document.addEventListener('DOMContentLoaded',function(event){
  // array with texts to type in typewriter
  var dataText = [ "> create", "> run", "> share"];
  
  // type one text in the typwriter
  // keeps calling itself until the text is finished
  function typeWriter(text, i, fnCallback) {
    // chekc if text isn't finished yet
    if (i < (text.length)) {
      // add next character to h1
     document.getElementById("anima").innerHTML = text.substring(0, i+1) +'<span aria-hidden="true"></span>';

      // wait for a while and call this function again for next character
      setTimeout(function() {
        typeWriter(text, i + 1, fnCallback)
      }, 100);
    }
    // text finished, call callback if there is a callback function
    else if (typeof fnCallback == 'function') {
      // call callback after timeout
      setTimeout(fnCallback, 1000);
    }
  }
  // start a typewriter animation for a text in the dataText array
   function StartTextAnimation(i) {
     if (typeof dataText[i] == 'undefined'){
        setTimeout(function() {
          StartTextAnimation(0);
        }, 2000);
     }
     // check if dataText[i] exists
    if (i < dataText[i].length) {
      // text exists! start typewriter animation
     typeWriter(dataText[i], 0, function(){
       // after callback (and whole text has been animated), start next text
       StartTextAnimation(i + 1);
     });
    }
  }
  // start the text animation
  StartTextAnimation(0);
});
</script>

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
![diy](/images/cmdr-ads.gif)
{{< /column >}}
{{< /block >}}
