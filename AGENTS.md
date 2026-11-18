# audio-test-fixtures

Shared audio fixture files consumed as a git submodule by `audiometa-python` and `hear-the-music-tree-api`. See `README.md`.

- Fixture names are part of consumer contracts: never rename or delete a file without updating every consumer. Some files are symlinks to identical content under another name; preserve them.
- Adding a fixture: commit it here, then bump the submodule gitlink in each consumer.
- No build or tests; consumers' suites validate the fixtures.
