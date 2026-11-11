# Driftwatch

An all-in-one, dependency-free HTML page showing how **Shannon entropy** and **KL divergence** can detect drift in infrastructure telemetry, with a focus on **the subject lines of a large fleet's tickets**.

Open `index.html` in a browser. No build step, no network access needed.

## What's inside

1. **The two ideas**: H(P) and D(P‖Q) in plain terms.
2. **Ticket subject drift (pipeline)**: normalize subjects into templates (hostnames, numbers, IPs, versions stripped), then histogram them. Includes an interactive normalizer.
3. **Live fleet ticket simulator**: 40 racks, ~3,000 tickets/day, 18 templates. A baseline is learned from 14 healthy days and thresholds are calibrated on 7 more. Inject incidents and compare volume, entropy and KL detectors (with detection lag): new firmware bug (new subject line), slow burn, rack power event, and a monitoring-tool rollout that changes subject formatting (false positive that normalization fixes). A ranked table shows which templates drive the KL, flags NEW ones, and reports rack spread (localized / cohort / fleet-wide).
4. **Bring your own tickets**: paste subject lines (processed locally in the browser) and get entropy, KL and the top contributing templates, baseline vs recent.
5. **Playground P vs Q**, 6. **Live traffic drift detector**, 7. **Load balancer evenness**: the underlying mechanics on other kinds of telemetry.
8. **Where this fits**: use-case table and practical notes.

All simulated data; nothing leaves your browser.

## License

MIT
