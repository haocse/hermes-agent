# hpins

Personal macOS helper scripts for Hao's Hermes Desktop workflow.

- `hpins`: prints Hermes Desktop pinned sessions first, then recent sessions. Titles are clickable terminal hyperlinks when supported.
- `hermes-session`: resumes a Hermes session in a right-side cmux split.
- `hermes-session-server`: local HTTP bridge for `hermes-session://resume/<id>` hyperlinks.

Install locally:

```bash
mkdir -p ~/.local/bin
cp scripts/hpins/hpins ~/.local/bin/hermes-pinned
cp scripts/hpins/hermes-session ~/.local/bin/hermes-session
cp scripts/hpins/hermes-session-server ~/.local/bin/hermes-session-server
ln -sf ~/.local/bin/hermes-pinned ~/.local/bin/hpins
```

The scripts are intentionally macOS/Hermes Desktop/cmux oriented and read pinned IDs from Electron LocalStorage at:

`~/Library/Application Support/Hermes/Local Storage/leveldb`
