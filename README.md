# A Short Guide to Cheese

CSE 134B — HW3: Introducing CSS Part 1 (Vocabulary)

Takes the plain text of `cheese.txt` and turns it into a semantic HTML page
with a hand-authored stylesheet. No frameworks, no JavaScript.

**Live site:** https://cheesearticle.netlify.app

## Files

| File | What it is |
|---|---|
| `cheese.html` | The page. Semantic markup — the tags are chosen based on what each chunk of text *is*, not how it looks. |
| `cheese.css` | All the styling. Imports `variables.css` at the top. |
| `variables.css` | The `:root` custom properties — colors, font stack, spacing value. |
| `_redirects` | Netlify config so the homepage serves `cheese.html`. |

## Notes

- Colors are an orange/yellow theme, written as `rgb()` values in
  `variables.css` so they can be changed in one place.
- `variables.css` is pulled in with `@import`. A `<link>` tag would be better
  in a real project since `@import` loads slower, but the assignment asked
  for `@import`.
- There's a small `<style>` block in the HTML `<head>` that overrides the `h1`
  color from `cheese.css` — that's the cascade demo, and the comment there
  explains why it wins.

## Running it locally

The `@import` can fail if you just double-click the HTML file, so use a local
server:

```
python -m http.server 8000
```

Then open `http://localhost:8000/cheese.html`. The Live Server extension in
VS Code works too.
