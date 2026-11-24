# dragonglass source: 5e, everything

The whole of 5etools' 2014 and 2024 data as [dragonglass](https://github.com/Apollo-XIV/dragonglass-builder)
content, setting prose (`fluff`) included, with mechanics the converter's LLM pass wrote
(`llm:claude-sonnet-5-5`, review `auto`, unverified).

**Private. Not for redistribution.** Unlike the SRD repos, this is published material that is not
CC-BY; keep it to local use.

## Layout

Two sources, one directory each, each with its own `source.json` and `content/`:

- `srd/` — the 2014 ruleset (source id `srd`), 5293 elements in 70 books
- `srd24/` — the 2024 ruleset (source id `srd24`), 3231 elements in 16 books

Each element's `source` is the book that printed it (`xge`, `tce`, `lfl`...), one `sourcebook`
element per book, so the builder tags an option with its book and can filter by it. Ids stay under
the source (`srd:spell:toll-the-dead`), so characters built before this keep resolving. What the
converter made itself, such as a species' traits or a proficiency set offered as an option, is in
the book that offers it, or the core rulebook (PHB, XPHB) when several books do.

Both validate at 0 errors, 0 warnings against the plugin's validator.

## Generated, not hand-edited

Built by 5etools-to-dragonglass with `npm run convert -- 2014 --fluff` and
`npm run convert -- 2024 --fluff`, then `npm run llm -- ask|apply`. Changes belong in the converter.
