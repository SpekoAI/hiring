# Measurement lane

Measurement gate (GATE-ENG-BENCH). You get this task after the written step on the page. Your due date and your review date arrive in the message that sends it.

Task: build a tiny English-voice benchmark harness we can run from a clean checkout and get your exact numbers, plus a short recorded defense.

Deliverable, one repo with a README:

1. Pick one axis: TTS or STT. Measure 2 real providers (your pick, English audio/text only) on the same fixed inputs.
2. Report latency p50 and p95 (for TTS: time to first audio byte, TTFB; for STT: end-to-end), plus one quality number (TTS: a stated subjective or objective proxy; STT: WER on a labeled English sample with jiwer or equivalent). Pin model versions and capture date. Commit the input fixtures and a seed so a re-run reproduces the numbers.
3. Write a "What this does not measure" section. Say plainly what the sample size is, what is noisy, and what you would never claim from this.
4. README: exact commands so we get your numbers from a fresh clone in under 10 min on a normal laptop, with one .env.example. No paid API key from us should be required to see the harness run (use a free tier, a recorded fixture, or a mock that is clearly labeled). Your reported numbers must come from real provider calls you made; a mock exists only so we can see the harness run without a key, and every output it produces must say it is a mock.
5. Record a 3-5 min screen video (English, your real voice) walking us through your numbers and answering: which provider is faster, why, and what would make this benchmark wrong. Talk like you are defending it to a skeptical engineer.

What passes, all five: (a) a fresh clone reproduces your p50 and p95 within noise in under 10 minutes, with no paid key from us; (b) latency reported as real percentiles, not a single mean and not a mock-only number labeled as real; (c) a "What this does not measure" section that names a real limitation of your own setup; (d) the quality number computed by your code, not copied from a vendor page; (e) a recorded defense in your own voice that survives one "why should I trust this number?" without inventing a figure. Any miss fails.

Scope it small. We care about reproducibility and plain reporting, not coverage. Apply through the form on [this page](README.md).
