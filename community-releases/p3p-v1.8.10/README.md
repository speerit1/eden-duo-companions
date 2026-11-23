# Persona 3 Portable — AYN Thor UI v1.8.10 FINAL

**Unofficial community mod** — independently tested, original completed design.

**Download:** [v1.8.10 FINAL (.dsmod.zip)](https://raw.githubusercontent.com/speerit1/eden-duo-companions/p3p-v1.8.10-release/community-releases/p3p-v1.8.10/0100DCD01525A000-Persona3PortableDS-v1.8.10-FINAL.dsmod.zip)

- Version: **1.8.10 FINAL** — the original working version, not the unfinished PR #31 source-port prototype
- ZIP SHA-256: `70faf618f1fd4777c78d5204688b5427e80eeb0e57c2d16ec30e9b02ed3e4513`
- Supported game: Persona 3 Portable, Switch 1.0.0, title ID `0100DCD01525A000`
- AYN Thor / Eden Duo dual-screen companion, minimum runtime 19
- 12 pages, 2,798 reader outputs, 61 defined actions, 62 procedurally styled PNGs
- No game ROM, keys, game dumps, game fonts or game music bundled

**Install:** back up any existing P3P companion; install this archive through Eden Duo's normal dual-screen mod process. Keep the original archive for rollback. Test Battle and game-state interactions on your exact emulator version.

**Documentation:** [release notes](RELEASE_NOTES.md) · [asset provenance and upstream integration](PROVENANCE_AND_UPSTREAM.md) · [asset inventory](ASSET_PROVENANCE.csv) · [manifest reference extractor](v1810_reference.py) · [procedural art generator](generate_art_v18_partial.py) · [asset hash verifier](verify_generated_31.py)

The exact final manifest is recorded here as a verified compressed text fixture for contributors. Run:

```sh
python3 community-releases/p3p-v1.8.10/v1810_reference.py --output /tmp/p3p-v1.8.10-manifest.json
```

**Credits:** original base companion by jschroeder1; Eden Duo Companions project maintained by igawa6; Thor redesign created and tested by community contributor with AI assistance from Claude (Anthropic) and ChatGPT (OpenAI).

**Licensing and limitations:** upstream source is GPL-3.0-or-later; image generation provenance is partly reconstructed, documented in the included inventory. The original module sources are available in the parent repo; exact binary/source reproducibility is still to be verified. This public release branch is **not a proposed upstream source change** and is intentionally separate from [draft PR #31](https://github.com/igawa6/eden-duo-companions/pull/31).

**Source recovery update:** The included procedural generator and verifier have reproduced **31 of the 62 bundled PNGs byte-for-byte**, confirmed against original v1.8.10 SHA-256 hashes using the locally installed Inter font. Generate and verify with `python3 generate_art_v18_partial.py --output /tmp/p3p-art` followed by `python3 verify_generated_31.py /tmp/p3p-art`. The other 31 assets still need their generation sources reconstructed or appropriately licensed before the upstream source PR can be considered complete.
