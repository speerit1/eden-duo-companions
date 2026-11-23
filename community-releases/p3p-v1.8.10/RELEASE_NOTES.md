# Persona 3 Portable — AYN Thor companion, v1.8.10 FINAL

**Status:** Community-tested original build. This is the definitive 1.8.10 visual design, *not* the incomplete PR #31 source-port preview.

This is an unofficial fan modification and is not affiliated with ATLUS, SEGA, Eden Duo or the original companion maintainer. It **does not contain the game ROM, game dumps, game music, saves, fonts or keys**. The two platform-specific `.so` modules read game resources at runtime; this release includes **62 custom UI graphics**, a 12-page manifest and the modules.

## Compatibility

- Game: Persona 3 Portable (Nintendo Switch), version **1.0.0**, title ID `0100DCD01525A000`, supported build ID documented by the upstream P3P source.
- Display: AYN Thor lower screen / Eden Duo dual-screen companion.
- Minimum companion runtime: **19**. Refer to upstream for emulator version compatibility.
- Android ARM64 and Linux x86-64 native modules included.

## Install and rollback

1. Back up an existing `0100DCD01525A000.dsmod.zip` or installed Persona 3 Portable companion. Do not install both variants at once.
2. Install the **v1.8.10 FINAL** `.dsmod.zip` through Eden Duo's supported dual-screen mod workflow.
3. Run the supported game and check Main, Skill, Persona and Items interactions; re-check Battle in actual combat.
4. If problems arise, reinstall the original saved companion archive.

## Verified on the supplied file

- ZIP CRC/integrity check, 67 entries, 12 pages, 61 actions, 2,798 game-state outputs, 62 PNGs.
- PNG resources and native modules included; file references can be checked by `v1810_reference.py`.
- Original ZIP **SHA-256:** `70faf618f1fd4777c78d5204688b5427e80eeb0e57c2d16ec30e9b02ed3e4513`.
- Original manifest **SHA-256:** `d9079a3852e24a24c07608ccfcb32b0b4c9c1283476650204e2a72cb30c9e379`.
- The release download is a **byte-identical copy** of the original v1.8.10 FINAL ZIP. The earlier PR #31 test ZIPs are **not** this release.

## Credits and source

- The base companion was originally developed by **jschroeder1** and contributed to the **Eden Duo Companions** project, maintained in [igawa6/eden-duo-companions](https://github.com/igawa6/eden-duo-companions).
- The UI redesign was iterated and tested by the community contributor with AI-assisted development using Claude (Anthropic) and ChatGPT (OpenAI).
- Native module corresponding source: [P3P module and build documentation](https://github.com/igawa6/eden-duo-companions/tree/main/tools/p3p) and [native module sources](https://github.com/igawa6/eden-duo-companions/tree/main/native/modules). This archive uses previously compiled binaries; exact binary-to-source reproducibility has **not** been independently demonstrated.
- Original upstream repository is licensed **GPL-3.0-or-later**; preserve source and copyright notices when redistributing. Images appear to be procedural rather than extracted game media, but generation provenance is partly reconstructed; see `ASSET_PROVENANCE.csv`.

## Known limitations

- **Battle** has not been exhaustively tested on real hardware in all enemy configurations.
- Some imagery is generated from earlier design stages, for which the original generation scripts have not all been recovered.
- Do not submit this whole binary archive into the upstream PR: that PR expects reproducible, asset-free source.
