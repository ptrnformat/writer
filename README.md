# Writer

Create and edit `.ptrn` files without writing code.

Planned home: [write.ptrnformat.org](https://write.ptrnformat.org) · Status: **planning**

## What it does

- Lets a designer enter a pattern through forms and editors, then saves it as a proper `.ptrn` file.
- Requires rows to be written in a set **row format**. Writer reads that format to work out the stitches. The format is defined once in [`ptrn-js`](https://github.com/ptrnformat/ptrn-js) and shared with Converter.
- Counts the stitches in each row and compares them with the designer's stated counts.
- Always tries to build the stitch graph. If counts don't match, it warns the designer and still lets them save a file that has only the written rows and no graph.
- Only saves files that pass the PTRN schema.
- Opens files made by [Converter](https://github.com/ptrnformat/converter) so the designer can finish them.

The hardest part is input: finding the simplest way for a designer to enter a pattern. That's where most of the design work goes.

## What it doesn't do

- **No judging the pattern.** Writer counts stitches so it can build the graph, and nothing more. Whether the pattern is good, or will fit, is up to the designer.
- **No AI.**
- **No viewing or printing for makers.** Use [Reader](https://github.com/ptrnformat/reader).

## How it works

- Browser-first. A server is added only if something can't be done in the browser.
- Crochet and knitting first. Specialty forms (Tunisian, loom knitting and so on) come later.

## Open questions

- **The row format.** What designers type for a row, how close it stays to how patterns are written today, and how it handles repeats, sizes and US/UK terms.
- **Optional graph in the spec.** The spec currently requires the stitch graph. It needs to allow a file with written rows only, for when counts don't match.
- **Draft flag.** Whether a file from Converter, or one saved without a graph, should be marked as a draft in the file itself.
- **Charts.** How designers enter charts, especially for knitting.
- **Knitting body.** The spec doesn't define a knitting body yet, so knitting support waits on the spec.

## Decisions

Decisions and the reasons behind them are logged in [DECISIONS.md](DECISIONS.md).

## License

[Apache 2.0](LICENSE)
