# Musinique YouTube Production Library

This repository contains non-MP3, non-MP4 production materials for two subjects only: Claude/Anthropic and independent music. It preserves beat sheets, visual assets, scripts, manifests, research notes, rendered stills, and quality-control artifacts for those projects.

The archive is designed for project discovery, editorial review, visual reuse, and reconstruction of video builds. Finished MP3 and MP4 media is intentionally excluded from version control.

## Collections

### `claude/`

The Claude-specific production archive. It includes collections explicitly about Claude, Claude Code, Claude Cowork, Anthropic, Claude prompt engineering, and Claude-related creative workflows. Content merely produced with Claude does not qualify when its subject is unrelated.

Broad AI, Codex, science, medicine, finance, mathematics, courses, and unrelated Claude-generated projects are outside this repository's scope. The collection currently contains 857 project folders and 1,237 beat-sheet files.

### `indie/`

Independent-music video concepts and builds, including series-level documentation and individual production folders. This collection contains 14 project folders and 21 beat-sheet files.

## Directory conventions

The archive has exactly two top-level content collections. Claude projects retain a clearly named Claude source collection when needed for provenance:

```text
claude/<claude-source-collection>/youtube/<video-slug>/
```

This hierarchy prevents same-named projects from overwriting one another and makes it possible to trace an asset back to the workspace that produced it.

General courses and educational projects belong in the Humanitarians YouTube repository. Medhavy holds its science collections.

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
5. Import only projects explicitly about Claude/Anthropic or independent music.
6. Do not commit final MP3 or MP4 renders to this repository.
7. Do not add general AI or course material solely because Claude helped produce it.

## Repository scope

This repository mirrors `books/musinique/youtube` from the Bear Textbooks workspace. Unrelated material belongs elsewhere, even when Claude was used to produce it. This is a production-material archive, not a finished-media feed or the Musinique public website.
