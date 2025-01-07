---
title: You can pass a callback to a ref
date: 2025-01-07T08:23:35.432Z
---

```ts
function scrollTo(el) {
  // On first render and on unmount there 
  // is no DOM element so `el` will be `null` 
  // so we need to check if it exists
  if (el) {
    el.scrollIntoView({ behavior: "smooth" });
  }
}

function List({ data }) {
  return (
    <ul>
      {data.map((d, i) => {
        const isLast = i === data.length - 1;

        return (
          <li
            key={d.name}
            ref={isLast ? scrollTo : undefined}
          >
            {d.name}
          </li>
        );
      })}
    </ul>
  );
}
```