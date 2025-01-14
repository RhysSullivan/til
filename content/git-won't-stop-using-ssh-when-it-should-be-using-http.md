---
title: Git won't stop using SSH when it should be using HTTP
date: 2025-01-14T05:32:37.307Z
---

Check your gitconfig, it's likely that you have the following in it

```
[commit]
   ui = auto
```