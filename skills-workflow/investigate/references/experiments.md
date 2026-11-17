# Experiments, performance, and diagnosis

Check whether execution is allowed. A request to analyze existing evidence does not authorize new benchmarks. When execution is allowed, inspect reusable results and infrastructure before building a new harness.

## Evaluate algorithms or performance

Define success using the user's priorities: valid solution coverage, result quality, latency, throughput, memory, or another outcome. Correctness and capability gates come before ranking performance. Keep failures and timeouts in the results; do not report only successful cases.

Choose representative workloads and important edge cases. State how fixtures differ from real workloads. Compare controlled configurations and include a baseline; separate algorithm changes from parameter/default changes. Record revisions, environment, inputs, commands, configurations, and raw outputs needed to repeat the experiment.

Measure the relevant stages separately when needed: setup, preprocessing, execution, and reuse across repeated calls. Account for warmup/caches and variability; repeat or alternate runs when those factors could change the conclusion. Do not add statistical machinery that the decision does not need.

Observe what the benchmark actually exercises. Use targeted profiling or counters to explain anomalies and test bottleneck claims. An end-to-end improvement does not by itself prove the proposed mechanism caused it. Distinguish standalone usefulness from incremental benefit when a method is added to a pipeline.

Report distributions or ranges where a single aggregate hides important behavior. Keep measured outcomes separate from extrapolation and complexity analysis. A fixture speedup does not establish production performance or semantic equivalence.

## Diagnose a discrepancy

Establish expected versus observed behavior and a reproducible case. Form plausible competing explanations; choose checks that distinguish them rather than accumulating confirming examples for the first theory.

Trace relevant execution and state, using focused instrumentation or controlled changes. Distinguish symptoms, mechanisms, and root causes. If reproduction fails, report the exact tested conditions, what remains plausible, and the missing evidence. Do not replace an unresolved diagnosis with an unrelated optimization.

Follow the shared restoration procedure for temporary changes. Retain the reproducible experiment and evidence in the designated locations.

Methodological basis: [active benchmarking](https://www.brendangregg.com/activebenchmarking.html) checks what a benchmark is actually measuring; [Google's troubleshooting guidance](https://sre.google/sre-book/effective-troubleshooting/) describes iterative hypothesis testing and common causal-reasoning failures.
