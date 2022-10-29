## Commander Docs & Chart Repo

Official Commander Charts Repo part of https://github.com/alfiankan/commander.

## How to contribute and publish your chart here ?
1. Fork this repo
2. Create New chart following chart template below.
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

3. make it sure the kind name of chart is not duplicated
4. put your file to `statis/charts` `https://github.com/alfiankan/commander-charts/tree/main/static/charts`
5. add your chart kind to `https://github.com/alfiankan/commander-charts/blob/main/static/charts/repo.chart.json` as name and add readable description
6. create pull request with branch name format `charts/<kind>` eg. `charts/kubernetes`
