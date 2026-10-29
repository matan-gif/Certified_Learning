# Master's Thesis in Trustworthy Machine Learning

Matan Mahlev, University of Copenhagen

Deploying machine learning models in high-stakes settings, such as medicine, calls for reliable predictions. When can a prediction be **guaranteed** to be correct, and how can we **prove** it?

In a framework introduced by Blum et al.[^1], a certificate is a small subset of training samples that forces the label of a given test point $x$: every classifier in the chosen hypothesis class that is consistent with those samples must assign the same label to $x$. A $b$-robust certificate preserves this agreement when up to $b$ training samples may be adversarially corrupted.

My thesis makes two main contributions:

1. **Bounding the cost of robustness.** In the corruption-free setting, the worst-case certificate size is governed by the hollow star number $s_0(\mathcal{H})$ of the hypothesis class $\mathcal{H}$. Its robust counterpart, $s_b(\mathcal{H})$, plays the same role when up to $b$ samples may be corrupted. Using a connection to Helly-type theorems with tolerance, I show that

   $$s_b(\mathcal{H}) \leq \eta\bigl(s_0(\mathcal{H}), b+1\bigr),$$

   where $\eta$ is the Erdős–Gallai extremal function for critical uniform hypergraphs. For fixed $s_0(\mathcal{H})$, this gives an upper bound of $O\bigl(b^{s_0(\mathcal{H})-1}\bigr)$, showing that the cost of robustness grows at most polynomially with the corruption budget $b$.
2. **Finding small certificates.** Given a hypothesis class $\mathcal{H}$, a training set $S$, and a test point $x$ certified by $S$, the learner's goal is to find a **smallest** subset of $S$ that certifies $x$. First, I show that this problem is exactly equivalent to a minimum hitting-set problem. Second, I give an oracle-based algorithm that is efficient in the sample size $|S|$ and achieves an $O(d \ln |S|)$-approximation, where $d$ is the VC dimension of $\mathcal{H}$.


[^1]: Avrim Blum, Steve Hanneke, Chirag Pabbaraju, and Donya Saless. *Proofs as Explanations: Short Certificates for Reliable Predictions*. arXiv:2504.08377, 2025. https://arxiv.org/abs/2504.08377
