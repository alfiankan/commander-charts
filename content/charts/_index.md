---
title: "Charts list"
weight: 1
---

<h1> Available Commander Charts <span id="total-chart"> </span></h1>
{{< tip >}}
It's doable to contribute and publish to official chart by pulling request to [https://github.com/alfiankan/commander-charts](https://github.com/alfiankan/commander-charts) using valid chart format. Fell's free {{< /tip >}}
<table id="charts">

    
</table>

<script>
fetch('https://alfiankan.github.io/commander-charts/charts/repo.chart.json')
    .then(response => response.json())
    .then(data => {
        
       const chartsTable = document.getElementById('charts')
       const chartsTotal = document.getElementById('total-chart')
       chartsTable.innerHTML += `<thead>
            <td>Name</td>
            <td>Description</td>
        </thead><tbody>
       `
       data.forEach(v => {
        chartsTable.innerHTML += `
        <tr>
            <td><a href="https://alfiankan.github.io/commander-charts/charts/${v.name}.chart.json" target="_blank">${v.name}</a></td>
            <td>${v.desc}</td>
        </tr>
        ` 
       })
       chartsTable.innerHTML += `</tbody>`
       chartsTotal.innerHTML = data.length ?? 0 
    });


</script>

