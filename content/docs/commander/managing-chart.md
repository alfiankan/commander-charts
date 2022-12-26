+++
title = "Managing Charts"
description = ""
weight = 3
+++

## Concept
Chart is file unit containing sets of terminal command templates or code snippets and their properties, saved in json format as follows

```json
{
  "kind": "git", // chart group name alphabet [A-Z] [a-z] with no space (yocan use underscore _ )
  "description": "commander for Git", // chart group description
  "charts": [ // collection of charts
    {
      "usage": "load test apache benchmark", // chart usage
      "cmdt": "ab -n {{total_req}} -c {{total_concurrent}} {{target_url}}", // command or snippet template, use {{template}} to define template replacable by prompt
      "type": "cmd",
      "prompt": [ // promp definition to replace cmdt template
        {
          "tmplt": "total_req", // template associated with cmdt without double curly bracket 
          "label": "total request", // prompter label or intructions
          "default": "10" // prompter default value 
        },
        {
          "tmplt": "total_concurrent",
          "label": "total concurrent",
          "default": "2"
        },
        {
          "tmplt": "target_url",
          "label": "url load test target",
          "default": "https://github.com/"
        }
      ] 
    },
    {
      "usage": "unarchive tar file eg. .tar.gz",
      "cmdt": "tar -xvf {{file_path}}",
      "type": "cmd",
      "prompt": [
        {
          "tmplt": "file_path",
          "label": "archive file path",
          "default": "mypath.tar.gz"
        }
      ]
    }
  ]
}
```

Charts are located on your home directory `~/.commander` by default. You can have more than one charts.
```bash
.
├── example_2.chart.json
├── example_3.chart.json
├── example_4.chart.json
├── example_5.chart.json
├── git.chart.json
└── mychart.chart.json

0 directories, 6 files
```

## Using self hosted charts repo
You can create own chart or use official published charts from `https://alfiankan.github.io/commander-charts/charts` or by host your on your own github pages.
1. create your chart following `chart.json format`.
2. push to github and create github page
3. try to access your chart json like `myrepo.github.io/mychart/mychart.json`
4. to download or share just tell and use commander command `cmdr get mychart -h=https://myrepo.github.io/mychart`





## Using main official Commander charts repo
1. you can download all available charts by running `cmdr get --all`
2. or just want to download single chart run `cmdr get <chart_name>`, see charts name list at [Charts](/charts)

{{< tip >}}

It's doable to contribute and publish to official chart by pulling request to [https://github.com/alfiankan/commander-charts](https://github.com/alfiankan/commander-charts) using valid chart format. {{< /tip >}}

