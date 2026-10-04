# Infrastructure lane

Infra gate (GATE-PLATFORM-CASE). You get this task after the written step on the page. Your due date and your review date arrive in the message that sends it.

Task: a small build, runnable from a clean checkout. Build a minimal voice-provider router: given a request, route to one of two TTS (or STT) providers based on a simple policy (for example, cheapest that meets a latency budget), record per-request latency, and expose one observability endpoint that returns p50/p95 latency and error rate per provider over the last N requests.

Use mocked or free-tier providers; we do not need real audio quality, we need the routing and measurement plumbing to be real and correct. README with run commands, one .env.example, and a short note on what you would add for production (concurrency, failover, cost caps). No paid API key from us should be required to see it run.

Record a 3-5 min screen video (English, your real voice) walking us through the router and the endpoint: why the percentiles are right, and what would make them wrong.

No voice background needed. We are testing whether you build correct, observable systems and reason about latency under load.

What passes, all four: (a) a fresh clone runs the router and the endpoint in under 15 minutes; (b) p50 and p95 are computed correctly, not a mean relabeled, and update as requests flow; (c) the routing policy changes behavior under different inputs; (d) the production note shows real systems reasoning. Fake or static metrics, or a router with one path, fail.

Scope it small: about one day of your time. Apply through the form on [this page](README.md).
