# Master Thesis in Trustworthy Machine Learning

Matan Mahlev, University of Copenhagen

Trustworthy machine learning needs predictions we can justify—even when some training data have been corrupted. My thesis studies how to support individual predictions with short, checkable proofs.

In the model introduced by Blum et al., a certificate is a small subset of training examples that forces agreement: every classifier in the chosen hypothesis class consistent with those examples must assign the same label to the test point. A robust certificate preserves this agreement even when we allow up to $b$ label errors.

My thesis makes two main contributions:

1. **Bounding the cost of robustness.** I bound how much certificates may need to grow to withstand corrupted labels. Using a connection to Helly-type theorems with tolerance, I bound the robust hollow star number in terms of its uncorrupted counterpart and the corruption budget. For a fixed uncorrupted hollow star number, the bound grows only polynomially with $b$.
2. **Finding small certificates.** I show that extracting a smallest certificate in the uncorrupted setting is exactly equivalent to the classical minimum hitting-set problem. This exposes the computational difficulty and provides tools for approximation. In particular, for hypothesis classes of VC dimension $d$, I obtain an $O(d\log n)$-approximation using polynomially many calls to a weighted learning oracle, where $n$ is the sample size.
