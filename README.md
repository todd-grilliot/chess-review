# Todd vs Claude Opus 5 — annotated game

A full game of chess played by typing moves into a chat window, with Claude Opus 5 playing Black.
No chess engine suggested moves to either side: Claude wrote itself a rulebook (legal moves only —
no evaluation, no search) and worked the moves out in prose.

Todd won in 45 moves. Claude survived one bad tactical moment on move 7, took the lead on material
at move 34, then lost the endgame to a pair of connected queenside pawns and resigned.

**Read it here: https://todd-grilliot.github.io/chess-review/**

The page is a single self-contained HTML file — no images, scripts or fonts loaded from anywhere else.
Step through all 89 half-moves; the commentary beside the board is quoted verbatim from what the two
players actually said at the time (93 direct quotes), and there's a running tally of every occasion
where Claude's own tooling caught an error it had already made out loud.

## Editing

`index.html` is the whole site. Edit it, then:

```sh
git commit -am "update" && git push
```

GitHub Pages rebuilds in under a minute.

One thing to keep if you edit the top of the file: the `<head>` block, and specifically
`<meta name="viewport" content="width=device-width, initial-scale=1">`. Without it, phones lay the
page out at a virtual 980px and scale everything down, which makes the text too small to read and
stops the mobile styling from applying at all.
