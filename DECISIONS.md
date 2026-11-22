# Decisions

Newest first. Each entry records what was decided and why.

## 2026-11-22 — Initial scope

- **Focus on simple input.** The biggest job is finding the easiest way for a designer to enter a pattern.
- **Required row format.** Rows must be written in a set format so Writer can read them reliably without AI. The format lives in `ptrn-js` so Converter uses the same parser.
- **Stitch counts are checked.** Writer counts stitches per row against the designer's stated counts. It needs those counts to build the stitch graph.
- **On a mismatch, warn and save without a graph.** The goal is for every file to have a graph, but a broken pattern shouldn't stop the designer saving their work.
- **No other pattern validation.** Beyond counts, the pattern's correctness is the designer's responsibility.
- **Separate from Converter.** Converter outputs a `.ptrn` file, and Writer opens it for finishing.
- **Crochet and knitting first,** because those are what the CYC standards and Ravelry cover.
