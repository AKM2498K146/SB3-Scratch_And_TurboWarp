# License

This repository is split into two components under different copyleft licenses,
chosen so that **both the source code AND the creative assets remain free under
network / SaaS use** (the "Network Services" clause).

| Component | Location | License |
|-----------|----------|---------|
| **Source code** (all `.js`, `.ts`, `.py`, build scripts, etc.) | `/` (source tree) | **GNU AGPL v3** — see [`LICENSE`](./LICENSE) |
| **Creative assets** (images, audio, video, 3D models, textures, fonts, text) | `assets/` (or wherever media lives) | **CC BY-SA-NS 4.0** — see [`LICENSE-ASSETS`](./LICENSE-ASSETS) |

## Why this combination

- **AGPL v3** covers the code and triggers its "Remote Network Interaction"
  obligation (§13): any modified version offered as a network service must make
  its Corresponding Source available. This is **official, well-established, and
  widely recognised**.
- **CC BY-SA-NS 4.0** covers the assets and adds an equivalent **Network
  Services** clause (Section 3(c)): making the assets, or a Derivative Work
  based on them, available remotely (SaaS / APIs / hosted offerings) requires
  you to provide the Corresponding Source (source assets, prompts, configs,
  scripts, build instructions) free of charge under a Compatible License.

  → The motivation is genuine: official CC BY-SA 4.0 **does not** trigger any
  obligation on pure SaaS / network use, which is precisely the gap BY-SA-NS
  was proposed to close.

## Important — read carefully

The statement that "BY-SA-NS lists GNU AGPL v3 as a Compatible License" is
**asserted by the BY-SA-NS proposal itself, NOT endorsed by Creative Commons**.
The official CC compatible-licenses list only recognises a **one-way**
compatibility between **CC BY-SA 4.0 → GPLv3**
(see https://creativecommons.org/share-your-work/licensing-considerations/
compatible-licenses); it does **not** list AGPLv3.

Practical implication:

- **Separate components (recommended, safe).** Keeping code (AGPLv3) and
  assets (BY-SA-NS) as clearly separated components, each obeying its own
  license, is the well-supported path.
- **Merged / conveyed as one work under AGPLv3.** This relies on the untested
  premise that AGPLv3 qualifies as GPLv3-compatible for the purpose of a CC
  ShareAlike derivative work. This has **not** been confirmed by CC and has
  **not** been tested in court. Obtain professional legal advice before relying
  on this scenario.

## What this means for you

If you **modify and self-host / SaaS** this project (code or assets), you must
make the Corresponding Source available to users interacting remotely — that is
the whole point of this setup.

## REUSE / SPDX annotations

Two helper files are provided so every asset carries a machine-readable license
notice (checked with `reuse lint`):

- **`.reuse/dep5`** — the standard DEP5-format annotation file.
- **`REUSE.toml`** — same information in the newer TOML format.

Both declare the custom reference `LicenseRef-CC-BY-SA-NS-4.0`, because
**CC BY-SA-NS has no official SPDX identifier** (it is not an official CC
license). The full license text always remains in `LICENSE-ASSETS`.

To use:

1. Install the `reuse` tool (`pip install reuse`).
2. Fill in `<year> <author>` in `.reuse/dep5` (and/or `REUSE.toml`).
3. For third-party assets, add one stanza per file preserving the upstream
   copyright and license.
4. Run `reuse lint` to verify every file is annotated.

## What you must fill in

- `<year> <author>` — your copyright line, in `LICENSE-ASSETS` and
  `.reuse/dep5` / `REUSE.toml`.
- The **NOTICE** block at the top of `LICENSE-ASSETS`: project title, creator,
  source URI, attribution text.
- The **THIRD-PARTY ASSETS** block in `LICENSE-ASSETS` if you include any
  third-party material (preserve upstream copyright notices).

## Disclaimer

1. `LICENSE-ASSETS` (CC BY-SA-NS) is **not an official Creative Commons
   license**; it is a proposed extension (BY-SA 4.0 + a Network Services
   clause). Creative Commons only publishes six license types (BY, BY-SA, BY-ND,
   BY-NC, BY-NC-SA, BY-NC-ND) and does **not** endorse BY-SA-NS. Its legal
   enforceability has not been tested in court.

2. **Compatibility warning.** The claim that BY-SA-NS is compatible with
   AGPLv3 is made by the BY-SA-NS proposal author, **not** by Creative Commons.
   The official CC position is that CC licenses are generally **incompatible
   with major software licenses**, with the sole exception of the one-way
   CC BY-SA 4.0 → GPLv3 compatibility. Whether AGPLv3 counts as GPLv3-compatible
   for the purpose of a CC ShareAlike derivative work is therefore an **open,
   untested question**.

   → **Recommended practice:** keep code and assets as clearly separated
   components, each under its own license. Only if you have obtained legal
   advice should you rely on conveying the combined work under AGPLv3.

Use at your own risk. Consult a lawyer before relying on this arrangement for
commercial distribution or enforcement.
