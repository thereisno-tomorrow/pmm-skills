# X access: Grok discovery, mirror evidence

Read when collecting X material. The [bundled helper](../scripts/x_access.py) is read-only, Python 3.10+ standard library only. An authenticated Grok CLI with public X search must already be available. It reuses the configured connection without reading credential stores. Executable resolution: `--grok`, `GROK_BIN`, PATH, then the current user's `.grok/bin/grok.exe`.

Run from the skill directory or replace the script location with its actual absolute path. Store outputs in the research workspace, outside the skill package. Use a new directory for each run:

```text
python scripts/x_access.py doctor
python scripts/x_access.py search --query "from:example RL environments" --lane founders --since 2025-01-01 --until 2025-12-31 --limit 10 --out research/x/search-founder-01
python scripts/x_access.py fetch --search-dir research/x/search-founder-01 --depth 3 --max-posts 40 --out research/x/corpus-01
```

The account/query is illustrative. Build public company/person/category queries from the brief; do not send private documents or internal context to Grok. Other lanes: `company`, `mentions`, `competitors`, `category`. Repeat `--search-dir` to combine searches while retaining every origin and deduplicating IDs. Target dissent, substantive replies, lower-reach voices and older date windows as appropriate. No claim of exhaustive search or complete timelines follows.

## Execution and evidence

1. `doctor` locates the executable only. A real search tests authentication and capability.
2. `search` records the exact public query/window/prompt and runs one bounded CLI invocation from an isolated temporary directory. Existing configuration/hooks remain; no bypass flags. Defaults: eight turns, 420 seconds, ten candidates (cap 25). Temporary work is retained, not recursively removed.
3. It parses the final posts array, discarding progress drafts, validates URLs/handles/dates, deduplicates and records rejections. Public response text and exposed usage are retained; runtime IDs, internal commentary and stderr contents are not. Launch failures, nonzero exits, timeouts, invalid responses and invalid results differ from a successful empty result.
4. `fetch` retrieves source text from the public FxTwitter API by ID, retaining raw payloads and retrieval times. It checks discovery author/date/window and strict excerpt fidelity. Quote retrieved text, even when Grok's mismatch is only typography.
5. Parent and quoted-post IDs are followed within explicit total-post/depth bounds, with in-run reuse and cycle detection. Depth three permits three context edges from a root. Bounds and inaccessible context remain visible. A 404 is an HTTP failure, not proof of deletion. Transient failures get at most one retry.
6. `index.md`, lane views, full source pages, `evidence.json`, raw responses and status form the collection. Roots are fetched before context so context cannot consume their budget. Lane views link canonical records rather than duplicate stores; source pages link to parent/quote pages. For large founder collections, author per-person reading views from canonical records.

Retrieve known posts with `fetch --url <public-status-URL> --out <new-directory>`; repeat `--url` if needed. Keep diagnostic controls separate from discovered results. Fetching upstream context does not enumerate downstream replies/quotes: use separate searches and disclose their limits.

## Inspect results and handle setup failures

Read `status.json`, `evidence.json` and search status before using the collection. Exit 2 indicates failure/partial results or invalid input. Partial records remain inspectable. A quotation mismatch alone need not invalidate a source; use source text. Author/date/window mismatches require review rather than acceptance. Retrieval is not relevance review: author keep/exclude/unresolved decisions after reading context.

If Grok is missing or cannot authenticate/search, report the specific failure and guide supported CLI setup. Do not inspect tokens, refresh cookies, install unrelated tools or invent results. A missing mirror response leaves an unverified lead; report it and continue with other authorized evidence where useful. Neither connection is assumed continuously available.

The helper supports public search, individual-post retrieval and upstream context recovery. It is a read-only client.
