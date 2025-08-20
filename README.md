# BSYB_Algorithm:
Built a vectorized Floyd–Warshall (APSP) pipeline that applies a boolean-style mask to the adjacency matrix and performs min-plus relaxation in a single broadcasted step per k-iteration. Absent edges are encoded via ∞ (or explicit bool masks), ensuring invalid paths are ignored without per-element branching. The suite benchmarks the tensorized PyTorch variant against a canonical NumPy triple-loop baseline with integrated timing, peak-memory profiling, accuracy checks (max finite-element diff), and seaborn visualizations across graph sizes.

Vectorized min-plus relaxation with broadcasted updates per k

Boolean-like masking via ∞ to gate unreachable paths

Reproducible graph generator (density, seed, weight range)

Unified timing and peak-memory profiling; accuracy verification

Automated sweeps over n with summary tables and plots

Clear performance–memory trade-off insights; modular, extensible design
