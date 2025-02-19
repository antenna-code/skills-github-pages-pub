---
layout: page
title: "Search"
permalink: /search/
---

<input type="text" id="search-input" placeholder="Search posts...">
<ul id="results"></ul>

<!-- Include the Simple-Jekyll-Search script (you can host it locally or via a CDN) -->
<script src="https://unpkg.com/simple-jekyll-search@latest/dest/simple-jekyll-search.min.js"></script>
<script>
  SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results'),
    json: '/search.json'
  });
</script>