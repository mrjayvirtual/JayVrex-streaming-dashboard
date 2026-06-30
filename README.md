JayVrex Streaming Performance Dashboard
Live: https://mrjayvirtual.github.io/JayVrex-Streaming-Dashboard/
The problem
Independent artists see vanity numbers (total streams) on most DSP dashboards, but not the metric that actually predicts whether a song has staying power: skip rate and completion rate, weighted by where the streams are really coming from.
What it does
An interactive dashboard that filters by platform (Spotify, Apple Music, Audiomack) and surfaces:
Total streams + saves + week-over-week growth
Stream-weighted skip rate (not a naive average — a 30K-stream track at 14% skip outweighs a 500-stream track at 40% skip)
Weekly growth trend, top listener cities, per-track breakdown
Process
Modeled the schema after real Spotify-for-Artists / Chartmetric export fields
Built a stream-weighted aggregation function for skip rate, instead of a plain average
Added live filtering (React useMemo) so the whole dashboard recalculates per platform
Designed the layout so the "exciting" number (streams) hooks attention, and the "real insight" number (skip rate) sits right under it
Stack
React, inline component state, no backend — pure front-end data modeling on sample data.
Note
Built with sample/synthetic data for demonstration. Not a Power BI file — a custom interactive dashboard built to show the same analytical thinking in a tool that runs anywhere, including mobile.
