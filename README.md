# audio-test-fixtures

Shared audio test fixture files, used as a git submodule by:

- [`audiometa-python`](https://github.com/BehindTheMusicTree/audiometa-python) at `audiometa/test/assets/shared`
- [`hear-the-music-tree-api`](https://github.com/BehindTheMusicTree/hear-the-music-tree-api) at `hear/test/utils/uploaded_track/files/shared`

These files were previously duplicated in both repos' histories (~604 MB each). This repo hosts
them once; consumers pin a commit via `.gitmodules`.

Some filenames are symlinks to another file in this repo with identical content, reflecting how
each consumer's test suite refers to the same fixture under a different descriptive name (e.g.
by bitrate, by size, by duration).

## Adding a new shared fixture

1. Add the file to this repo, commit, and push.
2. In each consumer repo, `cd` into the submodule directory, `git pull`, then commit the updated
   gitlink in the consumer repo.
