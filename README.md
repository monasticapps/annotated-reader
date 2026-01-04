# Annotated Reader

A single-page web app for reading annotated markdown documents with a Genius.com-style sidebar.

## Usage

1. Host `index.html` on any static web server (GitHub Pages, Netlify, etc.) or open it locally in a browser
2. Click "Select Folder" and choose a folder containing your annotated document
3. Click any highlighted term to view its annotation in the sidebar

## Folder Structure

Your content folder should contain:

```
my-document/
├── main.md          # Main document (required)
├── term1.md         # Annotation for [[term1]]
├── term2.md         # Annotation for [[term2]]
├── _Special Term_.md # Annotation for [[Special Term]]
└── image.png        # Images referenced in annotations
```

## Writing Content

**main.md** - Your main document with linked terms in double brackets:

```markdown
CHAPTER I
INTRODUCTION

This is about [[seriatim]] opinions and [[Fiat lux]] moments.
```

**Annotation files** - One `.md` file per term. The filename should match the term:
- `seriatim.md` for `[[seriatim]]`
- `_Fiat lux_.md` for `[[Fiat lux]]` (underscores for special characters)
- `my-term.md` for `[[my term]]` (hyphens for spaces also work)

Annotations support basic markdown: **bold**, *italic*, lists, and images.

## Features

- Clean, readable typography (Computer Modern serif font)
- Sidebar appears when clicking linked terms
- Press Escape or click outside to close sidebar
- Works entirely client-side (no server required)
