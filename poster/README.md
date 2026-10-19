# DualFaith poster

A0 portrait poster for *DualFaith at NLPCC-2026 Task 10*, summarizing both tracks.
Build it with XeLaTeX through `latexmk`:

```sh
make
```

The project-level `latexmkrc` also routes hosts that invoke `latexmk -pdf`
(including a project still configured for pdfLaTeX) through XeLaTeX, which is
required by `fontspec`.

The two system diagrams are stored in `assets/` and retain their original
aspect ratios.

Building requires **TeX Gyre Heros**. `fontspec` resolves it by font name, so on
macOS it must be installed as a system font — TeX Live's own copy is not visible
to Core Text. On Linux, pointing `OSFONTDIR` at the TeX Live font tree is enough.

Use `make clean` to remove intermediate files, or `make distclean` to also remove
the generated PDF. The original figure PDFs are retained.
