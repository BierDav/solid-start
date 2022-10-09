---
section: api
title: A
order: 1
subsection: Router
---

# A

```tsx
import { A } from "solid-start";

export default function Nav() {
  return (
    <nav>
      <A href="/about">About</A>
      <A href="/">Home</A>
    </nav>
  );
}
```

The `<A>` component is designed handle links for client-side routing. It is a wrapper of the `<a>` element and is a re-export from `@solidjs/router`. These components are progressive enhancible and can work with client-side routing even when not hydrated bridging the gap between Single Page applications and Islands.

The `<A>` tag also has an `active` class if its href matches the current location, and `inactive` otherwise. **Note:** By default matching includes locations that are descendents (eg. href `/users` matches locations `/users` and `/users/123`), use the boolean `end` prop to prevent matching these. This is particularly useful for links to the root route `/` which would match everything.

### A Props

<table>
  <tr><th>Prop</th><th>Type</th><th>Description</th></tr>
  <tr><td>href</td><td>string</td><td>The path of the route to navigate to. This will be resolved relative to the route that the link is in, but you can preface it with `/` to refer back to the root.</td></tr>
  <tr><td>noScroll</td><td>boolean</td><td>If true, turn off the default behavior of scrolling to the top of the new page.</td></tr>
  <tr><td>replace</td><td>boolean</td><td>If true, turn off the default behavior of scrolling to the top of the new page.</td></tr>
  <tr><td>state</td><td>unknown</td><td><a href="https://developer.mozilla.org/en-US/docs/Web/API/History/pushState" target="_blank">Push this value</a> to the history stack when navigating.</td></tr>
  <tr><td>activeClass</td><td>string</td><td>The class to show when the link is active.</td></tr>
  <tr><td>inactiveClass</td><td>string</td><td>The class to show when the link is inactive (when the current location doesn't match the link).</td></tr>
  <tr><td>end</td><td>boolean</td><td>If `true`, only considers the link to be active when the curent location matches the `href` exactly; if `false`, check if the current location _starts with_ `href`.</td></tr>
</table>