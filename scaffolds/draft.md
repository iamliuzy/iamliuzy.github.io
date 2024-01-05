---
title: {{ title }}
tags:
---



<link rel="stylesheet" href="https://unpkg.com/gitalk/dist/gitalk.css">
<script src="https://unpkg.com/gitalk/dist/gitalk.min.js"></script>
<div id="gitalk-container"></div>
<script type="text/javascript">
    var gitalk = new Gitalk({
      clientID: '6b425e84088235852a6e',
      clientSecret: 'e88427a81bccf5ac0f1737a1459305c446f254be',
      repo: 'blog-comments',
      owner: 'iamliuzy',
      admin: ['iamliuzy'],
      id: location.pathname,      // Ensure uniqueness and length less than 50
      body: location.href
      distractionFreeMode: false  // Facebook-like distraction free mode
    });
    gitalk.render('gitalk-container')
</script>