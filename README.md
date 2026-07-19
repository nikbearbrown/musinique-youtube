# Musinique YouTube Production Library

This repository contains the non-MP3, non-MP4 production materials collected under `books/musinique/youtube`. It preserves the beat sheets, visual assets, scripts, manifests, research notes, rendered stills, and quality-control artifacts used across Claude-focused and independent video projects.

The archive is designed for project discovery, editorial review, visual reuse, and reconstruction of video builds. Finished MP3 and MP4 media is intentionally excluded from version control.

## Collections

### `claude/`

The main Claude and AI production archive. It includes consolidated projects gathered from multiple books and production areas, while preserving their original relative paths beneath `claude/_collected/`. It also contains selected first-class Claude project folders maintained directly under `claude/`.

This collection contains approximately 155,000 files and more than 5,600 beat-sheet variants.

### `indie/`

Independent Musinique video concepts and builds, including series-level documentation and individual production folders. This smaller collection contains roughly 525 files and 21 beat-sheet variants.

## Directory conventions

The archive favors provenance over a flat directory layout. A typical collected path looks like:

```text
claude/_collected/<source-book-or-project>/youtube/<video-slug>/
```

Preserving this hierarchy prevents same-named projects from overwriting one another and makes it possible to trace an asset back to the workspace that produced it.

## Typical project contents

Depending on the production stage, a project may include:

- `beat_sheet.json` and voice-, brand-, or format-specific variants
- editorial files such as `FACTCHECK.md`, `PEDAGOGY.md`, `PROMPTS.md`, and `SHOTLIST.md`
- rendering and scene scripts
- clip manifests, timing JSON, and concatenation instructions
- image, SVG, diagram, and layout assets under `media/`
- `_qc/` frames, overview images, QC sheets, and audit reports
- source notes, receipts, citations, build prompts, status files, and logs

Some files are generated artifacts retained to make visual inspection and reconstruction possible. Not every project is independently runnable outside the larger Bear Textbooks toolchain.

## Finding projects

```bash
# Find a project by title fragment or slug
find claude indie -type d -iname '*constitutional*'

# List primary beat sheets
find claude indie -name 'beat_sheet.json'

# Search scripts and editorial material
rg -i 'agent|education|music|alignment' claude indie

# Find QC reports
find claude indie -type f \( -iname '*qc*' -o -iname '*audit*' \)
```

## Media policy

The root `.gitignore` excludes all `.mp3` and `.mp4` files. JSON or text metadata inside a directory named `mp3/` can still be tracked because it contains timing information rather than audio. Supporting formats such as PNG, JPEG, SVG, M4A, Markdown, JSON, and source code may be present when required by the production archive.

## Recommended workflow

1. Start with the project's beat sheet to understand the narrative sequence.
2. Read fact-check, source, pedagogy, and prompt documents before editing content.
3. Use manifests and timing files to map beats to assets.
4. Review QC frames and audit reports at full resolution.
5. Preserve source-relative paths when importing additional projects.
6. Do not commit final MP3 or MP4 renders to this repository.

## Repository scope

This repository mirrors `books/musinique/youtube` from the Bear Textbooks workspace. It is a production-material archive, not a finished-media feed or the Musinique public website.

