---
date: 2022-05-12 19:46:31
priority: 0
status: done
tags:
- markata
- None
- None
templateKey: task
title: css variables in markata
uuid: d3c53b0f-6a0b-49c0-ab9d-2556c90b6414
---

darkmode css from Salma's [post](https://dev.to/whitep4nth3r/light-and-dark-mode-in-just-14-lines-of-css-424e)

## Full Dark Mode

we need the root step done first!

``` css
:root {
  --color-bg: #000000;
  --color-fg: #ffffff;
}

@media (prefers-color-scheme: light) {
  :root {
    --color-bg: #ffffff;
    --color-fg: #000000;
  }
}

body {
  background-color: var(--color-bg);
  color: var(--color-fg);
}
```