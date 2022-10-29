---
title: "Charts list"
weight: 1
---

## Available Commander Charts

<table id="charts">

    
</table>

<script>
fetch('https://alfiankan.github.io/commander-charts/charts/repo.chart.json')
    .then(response => response.json())
    .then(data => {
        
       const chartsTable = document.getElementById('charts')
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

    });


</script>

