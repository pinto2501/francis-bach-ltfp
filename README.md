# Learning Theory from First Principles (Francis Bach)

My worked solutions to the exercises in Francis Bach's *Learning Theory from
First Principles*.

## 📄 Latest PDF

Every push to `main` auto-builds the PDF via GitHub Actions and publishes it
to the `latest` release:

**[⬇ Download the latest PDF](../../releases/download/latest/main.pdf)**

## Structure

```
main.tex              # master file — includes preamble + all chapters
preamble.tex          # packages, theorem environments, shared macros
refs.bib              # bibliography (if any)
chapters/
  ch01_intro.tex       # one file per chapter
  ...
figures/               # tikz / plots
```

## Building locally

Requires a TeX distribution (TeX Live / MacTeX) with `latexmk`:

```bash
latexmk -pdf main.tex
```

Or use [Tectonic](https://tectonic-typesetting.github.io/) for a faster,
self-contained build:

```bash
tectonic main.tex
```

## Adding a new chapter

1. Create `chapters/chXX_name.tex` following the pattern in
   `chapters/ch01_intro.tex` (`exercise` / `proof` environments).
2. Add `\input{chapters/chXX_name}` to `main.tex`.
3. Push and the PDF rebuilds automatically.

