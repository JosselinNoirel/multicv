# Multilingual CV

If you've ever wanted to have multi-lingual CVs without having to maintain many separate files, here's an idea.  Maintain one .dtx file and use DocStrip to generate separate .tex files.

Steps used to produce two CVs from one file:

```bash
luatex cv.ins
```

then use lualatex or pdflatex or whatever your engine on the .tex files.

The .dtx file relies on DocStrip's option mark-up.

```latex
%<opt>One liner
%<*opt>
Several lines
of text
%</opt>
```