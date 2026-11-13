# CSS Typography: Text Wrapping, Overflow, and Truncation

## 1. Single-Line Truncation with Ellipsis
Truncates text exceeding its container width with a clean `...`:

```css
.truncate-single-line {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  max-width: 100%;
}
```

---

## 2. Multi-Line Clamping with Ellipsis
Clamps text to an exact number of lines (e.g. 2 or 3 lines) across all modern browsers:

```css
.truncate-multi-line {
  display: -webkit-box;
  -webkit-line-clamp: 2; /* Number of lines */
  -webkit-box-orient: vertical;
  overflow: hidden;
}
```

---

## 3. Long Word and URL Breaking
Prevents long URLs, hashes, or compound words from overflowing narrow mobile cards:

```css
.break-long-words {
  overflow-wrap: break-word; /* Modern standard */
  word-break: normal;        /* Allows break only when needed */
  hyphens: auto;             /* Optional: adds hyphenation */
}
```

---

## 4. Optimal Line Length (Measure)
For comfortable reading, body paragraphs should ideally span between **45 and 75 characters per line**:

```css
.article-prose {
  max-width: 65ch;
  line-height: 1.7;
}
```
