# Driftwatch

An all-in-one, dependency-free HTML page that shows how **Shannon entropy** and **KL divergence** can detect problems in infrastructure telemetry.

Open `index.html` in a browser. No build step, no network access needed.

## What's inside

1. **The two ideas**: H(P) and D(P‖Q) in plain terms, and why they catch changes that RPS or error-rate alerts miss.
2. **Playground**: edit an observed distribution P and a baseline Q; see entropy, both KL directions, and per-bucket contributions. Shows the asymmetry of KL.
3. **Live drift detector**: simulated request stream with a sliding window, entropy and KL charts, an adjustable alert threshold, and injectable incidents (credential stuffing, path scanner, CDN failure, health-check flood).
4. **Load balancer evenness**: `D(P‖Uniform) = log₂N − H(P)`, evenness and effective node count.
5. **Where this fits**: use-case table and practical notes (smoothing, windows, seasonal baselines, cardinality, threshold selection).

All data is simulated.

## License

MIT
