# Certified Learning

**Master's Thesis in Trustworthy Machine Learning**

## Summary

A model's prediction at a test point $x^\star$ can be *certified* by a small subset of the training data that a verifier can check: any hypothesis consistent with that subset must give $x^\star$ the same label. A *$b$-robust* certificate still works when up to $b$ training examples have been corrupted (data poisoning).

The thesis covers two questions:

1. **Combinatorial bounds.** How large can a $b$-robust certificate need to be in the worst case? The bound is stated in terms of the hollow-star number $s_0(H)$ of the hypothesis class and the corruption budget $b$. The thesis proves $s_b(H) \le \eta(s_0(H), b+1)$, which grows polynomially in either parameter when the other is held fixed.
2. **Certificate extraction.** Given a training sample that certifies a prediction, can a shortest (or approximately shortest) certificate be found efficiently? The thesis develops this for the realizable case ($b = 0$).

## Files

| File | Contents |
|---|---|
| [`msc_thesis_certified_learning.pdf`](msc_thesis_certified_learning.pdf) | Full thesis |
| [`thesis_presentation.pdf`](thesis_presentation.pdf) | Presentation slides |
