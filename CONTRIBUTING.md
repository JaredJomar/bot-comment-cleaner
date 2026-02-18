# Contributing

Thanks for helping improve Bot Comment Cleaner. Comment scanning stays local; only public filter-data JSON is fetched for updates.

## Quick start
1. Fork the repo and create a feature branch.
2. Make your changes.
3. Run local tests: `node scripts/test-comments.js`
4. Open a PR with a clear description and examples.

## Test cases
- Add new examples to `tests/comments.json`.
- Include both spam and legitimate comments to reduce false positives.

## Filter updates
- Prefer updating `remote/filters-data.json` over hardcoding patterns in `filters.js`.
- Bump the `version` in `remote/filters-data.json` for each data change.
- If you add regex patterns, keep them tight and avoid false positives.
- When adding obfuscation handling, keep performance in mind.

## Style and safety
- Keep runtime network usage limited to the approved remote filter-data JSON.
- Avoid collecting or storing user data.

## Reporting issues
If you find a missed spam comment, please include:
- The exact comment text.
- Whether the spam text was a link or plain text.
- The site URL.
