---
layout: randomstring
date: 2024-08-22
showWordCount: false
showReadingTime: false
showViews: false
showPagination: false
---


<script>
  document.addEventListener('DOMContentLoaded', function() {
    // I'm not a web dev, fuck. TODO: Improve way
    const urls = [
        '/posts/skhh',
      // moar
    ];    
    const randomUrl = urls[Math.floor(Math.random() * urls.length)];
    window.location.href = randomUrl;
  });
</script>
