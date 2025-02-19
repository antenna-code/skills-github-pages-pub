---
layout: page
title: "NOAA Data"
permalink: /noaa/
---

## Current Weather Data

<div id="noaa-weather">
  Loading NOAA ACE SWE data...
</div>

<script>
  // Fetch the latest 1-hour average data from NOAA
  fetch('https://services.swpc.noaa.gov/json/ace/swepam/ace_swepam_1h.json')
    .then(response => response.json())
    .then(data => {
      if (data && data.length > 0) {
        // Assuming the first object is the most recent reading:
        const latest = data[0];
        const container = document.getElementById('noaa-weather');
        container.innerHTML = `
          <h3>NOAA ACE SWE Data (1-hour average)</h3>
          <p><strong>Time:</strong> ${latest.time_tag}</p>
          <p><strong>Density:</strong> ${latest.dens}</p>
          <p><strong>Speed:</strong> ${latest.speed}</p>
          <p><strong>Temperature:</strong> ${latest.temperature}</p>
        `;
      } else {
        document.getElementById('noaa-weather').innerText = 'No data available.';
      }
    })
    .catch(error => {
      console.error('Error fetching NOAA data:', error);
      document.getElementById('noaa-weather').innerText = 'Failed to load NOAA data.';
    });
</script>