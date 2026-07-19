# Musinique — CLI Video Ideas ("X with Claude")

**Lane classification:** RESEARCH+BUILD — Mixed. The book title "Musinique" and its single substantive chapter (Chapter 1, currently a placeholder) suggests a music + AI topic. Based on the frontmatter and fundamental-themes chapter (which is the same Frictional/Phase Gates/Humans+AI framework shared across the Bear Brown series), this book appears to apply that framework to music creation, music theory analysis, or music education with AI. The chapter content is placeholder — all cards are derived from the stated subject matter and series context.

**Note on content state:** The main chapter (02-chapter-01.md) is a placeholder with no content yet. Cards are written for the stated topic (Music + AI) at BUILD/RESEARCH classification based on subject matter.

## Candidate 01 — "Research Music Theory Analysis with Claude: How AI Hears Chord Progressions"
- Source: musinique/chapters/02-chapter-01.md (stated topic: music + AI); musinique/chapters/97-fundamental-themes.md
- Lane: RESEARCH (Claude assistant)
- Hook: Claude can identify a ii-V-I jazz cadence, name the voice-leading logic, and explain why the tritone substitution works — but it cannot tell you whether it sounds good. The boundary between music theory analysis and aesthetic judgment is the exact phase-gate the series is built around.
- The artifact: A sourced 3-panel research brief: (1) Functional harmony — Claude analyzes a 4-bar chord progression (Cmaj7 → Fm7 → Bb7 → Ebmaj7) and identifies the modulation, the tritone substitution, and the voice-leading motion; (2) The analysis-vs-judgment boundary — where Claude's output is checkable (Roman numeral analysis, voice-leading intervals) vs. where it is opinion (whether the progression is "effective"); (3) A table of what music-theory tasks Claude can execute reliably vs. where a musician's ear is irreplaceable.
- Prompt seed: `claude "Analyze this chord progression: Cmaj7 → Fm7 → Bb7 → Ebmaj7. Provide: (1) Roman numeral analysis in the home key; (2) identify the modulation target if any; (3) name the voice-leading motion in each voice across the Bb7→Ebmaj7 resolution; (4) identify if this contains a tritone substitution and explain the substitution logic. Flag any claim where music theory analysis is ambiguous or where multiple valid analyses exist."`
- Read / check: Verify the Bb7→Ebmaj7 tritone substitution (Bb7 as a tritone substitute for E7, which would be V7 in A — or verify the analysis in the key of Eb); confirm that the voice-leading motion (Bb→Bb, D→Eb, F→G, Ab→Bb) follows standard smooth voice-leading; check that Roman numerals are correct for the stated home key.
- Human supplies: The chord progression input (human selects a musically interesting progression to analyze); screen-recording of the analysis session. A musician/music theorist to verify the analysis output.
- Output medium: screen-recording mp4
- The change: Follow-up: add the constraint "now analyze the same progression as if you are a jazz musician hearing it for the first time — what is the functional narrative, and where does tension resolve?" and compare the analytical vs. narrative outputs.
- Teardown angle: Music theory analysis is a Tier 1 task — pattern matching on well-established rules. Aesthetic judgment is Tier 7 — knowing what makes the music work for a listener. Claude can do the first reliably and the second only in the sense of pattern-matching what critics have written. The phase gate is the ear.
- Exclusions: Audio synthesis or MIDI generation; full music history; spectrogram analysis requiring audio files.
- Score: 8/10

## Candidate 02 — "Build a Chord Progression Generator with Claude: Functional Harmony as Code"
- Source: musinique/chapters/02-chapter-01.md (music + AI topic); series BUILD lane
- Lane: BUILD (Claude Code)
- Hook: The ii-V-I is the foundation of jazz harmony. If you know the rules — secondary dominants, tritone substitutions, modal interchange — you can generate an infinite set of valid jazz progressions. Claude Code can build the generator in 40 lines.
- The artifact: A Python script that accepts a root key and style (jazz, pop, classical) and outputs a chord progression with Roman numeral analysis and suggested voice-leading. A Manim animation of the output: a staff with chord symbols sweeping in, voice-leading arrows connecting chord tones across changes, and a color-coded functional analysis (tonic / subdominant / dominant roles).
- Prompt seed: `claude "Write a Python script: given a root key (e.g., 'C') and style ('jazz'), generate an 8-bar chord progression using functional harmony rules (ii-V-I, secondary dominants, tritone substitutions for jazz). Output the progression as: bar | chord symbol | Roman numeral | function (T/SD/D). Include at least one tritone substitution and one secondary dominant in the jazz output."`
- Read / check: Verify the tritone substitution logic (dominant 7th chord whose root is a tritone away from the standard dominant); confirm Roman numerals are correct for the generated key; test that the secondary dominant resolves to the correct target chord; check that the progression ends on a tonic cadence.
- Human supplies: Nothing — fully synthetic. The theory rules are analytic. A musician to assess whether the generated progression is musically interesting (the aesthetic judgment the script cannot supply).
- Output medium: Manim (animated)
- The change: Add a style parameter: "modal jazz" (using Dorian or Lydian modes) — generate a progression that avoids the V7→I motion and instead uses parallel motion or planing, and animate the difference in harmonic tension.
- Teardown angle: Functional harmony rules are code. The generator produces valid progressions mechanically — but validity is not the same as musicality. Claude Code can execute the theory; the musician's ear decides if the output is worth playing. The phase gate is the listen.
- Exclusions: Audio synthesis/playback; music notation rendering (LilyPond); stylistic variation beyond basic functional categories.
- Score: 8/10

## Candidate 03 — "Research AI Music Generation History with Claude: From Markov Chains to Transformers"
- Source: musinique/chapters/02-chapter-01.md (music + AI topic)
- Lane: RESEARCH (Claude assistant)
- Hook: Music AI has a 70-year history that most practitioners don't know: Hiller's Illiac Suite (1957) used Markov chains; Cope's EMI generated Bach-style pieces that fooled experts; Magenta's MusicTransformer introduced long-range attention for music. Claude can synthesize the timeline — but will it hold the evaluation disputes correctly?
- The artifact: A sourced 5-event timeline: Year | System | Technical approach | What it achieved | What critics disputed — covering Illiac Suite (1957), EMI (1981-2004), MIDI-RNN (2016), Magenta MusicTransformer (2018), and MuseNet/Suno (2019-2024). Generated by Claude with a challenge on the EMI Cope controversy (were the pieces genuinely "creative" or pattern-matching?).
- Prompt seed: `claude "Produce a sourced timeline of AI music generation: (1) Hiller/Isaacson Illiac Suite 1957, (2) David Cope's EMI system 1981-2004, (3) Google Magenta MusicTransformer 2018, (4) OpenAI MuseNet 2019, (5) Suno/Udio 2024. For each: technical approach, what it achieved, and the primary dispute about whether it constitutes 'musical creativity.' Cite primary sources where available. Flag any achievement claim that is disputed or hard to verify."`
- Read / check: Verify the Illiac Suite 1957 date and Markov chain approach; confirm the Cope EMI blind-study controversy (2010 confrontation with composer Steve Larson at University of Oregon); check that MusicTransformer's attention mechanism is correctly described; verify Suno/Udio are correctly identified as 2024 commercial systems.
- Human supplies: Screen-recording of the research session; a music theorist to assess whether the Cope/EMI "creativity" framing is fair.
- Output medium: screen-recording mp4
- The change: Follow-up: "The Cope/EMI controversy — does the fact that experts were fooled mean the music was creative, or does it mean the Turing test is the wrong criterion for creativity? Find me the strongest argument on each side."
- Teardown angle: The question "is AI music creative?" has been contested for 70 years. The technical capability improved from Markov chains to transformers; the philosophical question is unchanged. Claude synthesizes the technical history fluently; the creativity question is Tier 7 — requiring a self with aesthetic stakes.
- Exclusions: Music copyright law (Suno/Udio lawsuits); full transformer architecture; audio generation vs. symbolic generation distinction details.
- Score: 7/10

## Candidate 04 — "Build a Lyric Analysis Tool with Claude: Meter, Rhyme Scheme, and Prosody"
- Source: musinique/chapters/02-chapter-01.md (music + AI topic)
- Lane: BUILD (Claude Code)
- Hook: Songwriting has rules that most writers follow intuitively: syllable stress (iambic, trochaic), rhyme scheme (ABAB, AABB), and prosody — the match between speech stress and melodic rhythm. Claude can analyze all three in under a minute, flagging lines where the stress pattern fights the melody.
- The artifact: A Python script that accepts lyric text and outputs: (1) syllable count per line, (2) detected stress pattern (iambic/trochaic/etc.), (3) rhyme scheme label, (4) prosody alert if stressed syllables fall on melodically weak beats (requires a basic melody input as note sequence). A Manim visualization of the lyric annotated with stress marks and rhyme-scheme color coding.
- Prompt seed: `claude "Write a Python script that analyzes song lyrics for: (1) syllable count per line using CMU Pronouncing Dictionary; (2) dominant stress pattern (iambic, trochaic, dactylic, anapestic); (3) end-rhyme scheme labeled ABAB etc.; (4) flag lines where the syllable count breaks the dominant meter. Input: a verse of lyrics as a string. Output: annotated line-by-line table."`
- Read / check: Verify the CMU Pronouncing Dictionary is used correctly (pip install pronouncing); test on a known iambic pentameter line (Shakespeare) and confirm correct detection; check that rhyme scheme detection handles imperfect rhymes (near-rhymes); verify the meter-break flag fires on a deliberately irregular line.
- Human supplies: A set of song lyrics to analyze (human selects a real song verse — cannot use copyrighted material in the video without license consideration; use public-domain or self-authored lyrics); screen-recording of the script running.
- Output medium: screen-recording mp4 + Manim (animated lyric annotation)
- The change: Add prosody analysis: input a simple MIDI melody (note pitches and durations) and flag where stressed syllables land on metrically weak beats — the most common songwriting prosody error.
- Teardown angle: Lyric analysis is pattern-matching on pronunciation databases and rhyme rules — Tier 1. Whether a meter-break is an expressive choice or an error is Tier 7 — the songwriter's aesthetic judgment. The tool flags; the writer decides.
- Exclusions: Semantic meaning analysis; emotional sentiment scoring; full music theory of prosody across different languages.
- Score: 7/10

## Candidate 05 — "Research Music Education AI with Claude: Does Practice-with-AI Produce Real Musicianship?"
- Source: musinique/chapters/97-fundamental-themes.md (Frictional principle applied to music); musinique/chapters/02-chapter-01.md
- Lane: RESEARCH (Claude assistant)
- Hook: The Medhavy/Bastani finding for math education has a music education analog: an app that generates "perfect" accompaniment for a student's practice removes the productive struggle of listening, adjusting, and self-correcting — the neural events that build musicianship. Does the music education literature support this?
- The artifact: A sourced 2-section research brief: (1) What music practice research says about productive struggle (deliberate practice literature — Ericsson 1993 applied to music; Sloboda's research on musical expertise); (2) What AI music tools actually do to practice (rhythm correction apps, auto-accompaniment, AI feedback systems) and whether any published evidence shows whether they help or harm long-term musicianship.
- Prompt seed: `claude "Research the intersection of deliberate practice theory (Ericsson 1993) and music education AI tools. Summarize: (1) what deliberate practice requires in music learning specifically — what is the 'struggle' in instrumental practice? (2) For at least two AI music practice tools (rhythm apps, auto-accompaniment, AI feedback), what does published evidence say about whether they support or undermine the development of musical ear and self-correction capacity? Flag any effect-size claim you cannot verify."`
- Read / check: Verify Sloboda's research on musical expertise (The Musical Mind, 1985, or Exploring the Musical Mind, 2004); check if any peer-reviewed evidence on music AI practice tools exists (the literature may be sparse — Claude should flag this); confirm Ericsson's deliberate practice framework is correctly applied to music rather than just sports.
- Human supplies: Screen-recording of the research session; a music educator to assess whether the Ericsson framework applies cleanly to musical skill development.
- Output medium: screen-recording mp4
- The change: Follow-up: "If a rhythm correction app removes the struggle of subdividing beats internally, what specific musical capacity is at risk — and what practice design would preserve it while still using the tool?"
- Teardown angle: The Frictional principle applies to music as directly as to math. An app that corrects your rhythm in real time removes the listening loop — the moment when you hear your error and your brain encodes the correction. The productive struggle in music practice is irreplaceable; AI should make it more efficient, not eliminate it.
- Exclusions: Music copyright and AI generation legal disputes; specific app reviews; conservatory curriculum design.
- Score: 7/10

## Candidate 06 — "Build a Music Similarity Analyzer with Claude: What Makes Two Songs Sound Alike?"
- Source: musinique/chapters/02-chapter-01.md (music + AI topic)
- Lane: BUILD (Claude Code)
- Hook: The Blurred Lines lawsuit turned on whether a song could "feel like" another song without copying notes. Claude Code can compute the measurable components of musical similarity — key, tempo, chord progression, rhythmic pattern — and show exactly where two songs overlap and where they differ.
- The artifact: A Python script that accepts two chord progressions, tempos, and key signatures, and outputs: (1) key relationship (same key, relative major/minor, parallel, distant); (2) chord progression similarity (Levenshtein distance on Roman numeral sequences); (3) tempo ratio; (4) a similarity score from 0–1 based on the weighted combination. A Manim visualization of the two progressions side-by-side with similarity annotations.
- Prompt seed: `claude "Write a Python script that compares two songs given: key, tempo (BPM), and chord progression as Roman numerals. Output: (1) key relationship (same/relative/parallel/distant); (2) chord progression Levenshtein distance; (3) tempo ratio (faster song / slower song); (4) a weighted similarity score 0-1. Test on: Song A (C major, 120 BPM, I-V-vi-IV) vs. Song B (G major, 116 BPM, I-V-vi-IV)."`
- Read / check: Verify that the Levenshtein distance on Roman numeral sequences correctly handles transposition (I-V-vi-IV in C vs. I-V-vi-IV in G should have distance 0 if transposed, non-zero if literal); check the key-relationship classification (C major and G major are a perfect fifth apart — "close related"); confirm the test case similarity score is high (nearly identical progressions and tempos).
- Human supplies: Two song examples for the demo (can use well-known pop songs with the same I-V-vi-IV progression — Axis of Awesome example); screen-recording of the script running.
- Output medium: screen-recording mp4 + Manim (animated)
- The change: Apply the analyzer to three "Blurred Lines vs. Got to Give It Up" comparison dimensions (groove feel excluded since it requires audio) and show which computed dimensions are similar vs. dissimilar — making the legal analysis concrete.
- Teardown angle: Musical similarity has measurable components (key, harmony, rhythm) and unmeasurable ones (groove, feel, timbre, emotional resonance). Claude Code computes the former precisely. The latter is why courts need musicologists rather than algorithms — and why the Tier 7 judgment belongs to the human expert.
- Exclusions: Audio analysis (requires librosa/audio files); full musicological analysis of specific lawsuits; copyright law.
- Score: 6/10

## Candidate 07 — "Research Music AI Ethics with Claude: Who Owns a Song Co-Created with an AI?"
- Source: musinique/chapters/02-chapter-01.md (music + AI topic); chapters/97-fundamental-themes.md
- Lane: RESEARCH (Claude assistant)
- Hook: Suno and Udio generate full songs from text prompts. The US Copyright Office has ruled that purely AI-generated content is not copyrightable — but what about a human who edits 30% of the output? The law is being written in real time.
- The artifact: A sourced 3-section research brief: (1) Current US copyright law on AI-generated works — the 2023 Copyright Office guidance and the Thaler v. Perlmutter case; (2) The human-authorship threshold debate — what level of human creative input qualifies for copyright; (3) The music-specific dimension — sampling law, derivative works, and how Suno/Udio lawsuits (RIAA vs. Suno, 2024) are testing the boundaries.
- Prompt seed: `claude "Research the current legal status of AI-generated music. Summarize: (1) the US Copyright Office 2023 guidance on AI-generated works and what 'human authorship' requires; (2) the Thaler v. Perlmutter case outcome and its implications; (3) the RIAA lawsuits against Suno and Udio filed in 2024 — what the claims are and what legal theory is being tested. Flag any claim where the law is actively being litigated and the outcome is uncertain."`
- Read / check: Verify the 2023 Copyright Office guidance date and the Thaler case outcome (district court ruled AI cannot be named as author, 2023); confirm the RIAA lawsuit against Suno and Udio was filed in 2024; check that the "human authorship threshold" framing is accurate to current legal debate, not speculation.
- Human supplies: Screen-recording of the research session; a lawyer or legal commentator to review the legal framing (Claude should flag that it is not providing legal advice).
- Output medium: screen-recording mp4
- The change: Follow-up: "If a songwriter uses Suno to generate 20 variations, selects one, edits the melody and changes the lyrics completely — does that meet the human authorship threshold? What specific evidence would a court need?"
- Teardown angle: The law is catching up to the technology. The human authorship threshold is not a technical question — it is a values question about what creative contribution means. Claude synthesizes the current legal landscape fluently; it correctly cannot predict outcomes in live litigation. The Tier 7 judgment belongs to courts, not models.
- Exclusions: International copyright law; full RIAA complaint document analysis; music licensing detail.
- Score: 6/10

## Candidate 08 — "Build a Musical Key Detector with Claude: Finding the Tonal Center from Chord Symbols"
- Source: musinique/chapters/02-chapter-01.md (music + AI topic)
- Lane: BUILD (Claude Code)
- Hook: Given any chord progression, what key is it in? The Krumhansl-Schmuckler key-finding algorithm computes a correlation profile between chord tones and expected key profiles — and it can be implemented in 30 lines of Python.
- The artifact: A Python script implementing the Krumhansl-Schmuckler algorithm: accepts a list of chord symbols, converts to pitch-class frequency vectors, correlates with major and minor key profiles, and returns the top 3 key candidates with confidence scores. A Manim animation of the pitch-class distribution and the key-profile correlation sweeping across 24 possible keys, landing on the best match.
- Prompt seed: `claude "Implement the Krumhansl-Schmuckler key-finding algorithm in Python: (1) accept a list of chord symbols; (2) convert to a 12-bin pitch-class frequency histogram (count all notes in all chords); (3) correlate the histogram with Krumhansl's major and minor key profiles; (4) return the top 3 key candidates with Pearson r scores. Test on: [Cmaj7, Am7, Dm7, G7] (expected: C major)."`
- Read / check: Verify the Krumhansl key profiles are from the 1990 Cognitive Foundations of Musical Pitch book; test that the algorithm correctly identifies C major for the test input; confirm the Pearson correlation is computed correctly and A minor is close behind C major for the given input; check that the pitch-class histogram is correctly built from chord symbols.
- Human supplies: Nothing — fully synthetic (key profiles are published constants). A musician to verify the test cases.
- Output medium: Manim (animated)
- The change: Test on an ambiguous progression (F major: Fmaj7 → Bbmaj7 → Gm7 → C7 — could be F major or Bb major/G Dorian) and show the algorithm's confidence scores for multiple keys, making ambiguity visible.
- Teardown angle: Key detection is a pattern-correlation problem — Tier 1. The Krumhansl algorithm is from 1990; modern ML key detectors are more accurate on audio but still fail on ambiguous or modal music. The algorithm makes the statistical basis explicit: key detection is measuring which template your pitch content correlates with most.
- Exclusions: Audio-based key detection (requires librosa); microtonal tuning systems; modal mixture analysis.
- Score: 6/10
