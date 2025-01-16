---
title: How to make Cursor use the context of multiple repos at the same time
date: 2025-01-16T02:57:02.953Z
---

Put the repos in the same folder, open the folder containing the repos, and then make a .code-workspace file to open them in

```json
{
    "folders": [
      {
        "path": "frontend"
      },
      {
        "path": "backend"
      }
    ]
  }
```

The benefit here is it lets you keep the context across repos, so Cursor will be able to do inference from your open backend/ files while you work in frontend/