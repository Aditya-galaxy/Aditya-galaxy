## Aditya Kumar

Software Engineer and Researcher. I build systems that act on evidence, and I care most about measuring whether they are right.

---

### Research

**[protein-binder-design](https://github.com/Aditya-galaxy/protein-binder-design)**: can computational geometry and inverse folding generate functional de novo miniprotein binders against therapeutic cancer checkpoints without wet-lab screening?
Designed 3-helix bundle scaffolds targeting the human PD-1/PD-L1 checkpoint interface (PDB 4ZQK). Using SE(3) rotation alignment to biological hotspots (Tyr56, Gln66, Met115) and a ProteinMPNN inverse-folding decoder with a 3-residue autoregressive repetition penalty, lead candidates achieve pLDDT 93.6, ipTM 0.731, ΔSASA 889 Å², and shape complementarity $S_c$ 0.662 with zero steric clashes.

**[gb1-fitness](https://github.com/Aditya-galaxy/gb1-fitness)**: can a model trained on simple protein variants predict complex ones, and does it know when it is wrong?
On the GB1 fitness landscape, neural networks beat an additive model only when training data already contains combinations of mutations, and their ensemble uncertainty carries no signal when they have to extrapolate. Protein language model features (ESM-2) lift the hardest case from 0.55 to 0.75 (a BLOSUM62 control shows half of that is amino-acid similarity alone). Bayesian active learning (Expected Improvement) discovers the global optimum quadruple mutant `FWAA` within 240 assays (<2.8% of library), while 3D structural analysis links the strongest 2nd-order non-additive epistasis (coupling 4.31) to sub-4 Å physical proximity across the antiparallel β-hairpin contacting antibody Fc.

**[nuclei-shift](https://github.com/Aditya-galaxy/nuclei-shift)**: does a cell segmentation model know when a microscope image is unlike its training data?
Cellpose's nucleus model scores zero on stained tissue and brightfield images, and inverting brightness recovers most of it. Its confidence flags its own failures almost perfectly, while the generalist model stays confident while failing. Fine-tuning on up to 50 annotated images did not catch up with the one-line fix. Also run as a Cloud Run batch job: $0.65 per 1,000 images.

**[openvitals](https://github.com/Aditya-galaxy/openvitals)**: open, validated sleep and recovery algorithms for wrist wearables, and a benchmark that keeps them honest.
A heart-rate-only ensemble (5 TCNs + 5 GRUs, a 1 MB ONNX file) stages sleep at kappa 0.51 on a cohort it never saw, near commercial-watch level, and `openvitals stage` runs it on Apple Health, Gadgetbridge or CSV exports. On 100 sleep-clinic patients with a different wristband, the same model halves to 0.24: the benchmark's main finding is that headline accuracy doesn't transfer across people and devices. Wrist HRV against ECG has a 16% nightly error and ranks people well, but reads about 28% high, so it's reported as a personal trend, not an absolute value.

#### Built and shipped

- **[noscam](https://github.com/Aditya-galaxy/noscam)**: Antivirus for scams. 2nd place, TLN Cybersecurity Challenge 2026.
- **[recap](https://github.com/Aditya-galaxy/recap)**: Screen recorder for Mac, Windows and Linux. Turns recordings into ready-to-post videos.

#### Work

Software Development Engineer Intern at **Matter** (2026): Built a distributed event streaming system in Rust and Python, peaking above 60K TPS. Contributed to backend product development and auth service, Java spring boot.

#### Tools

Python, Rust, C++, Java, SQL · PyTorch, Biopython, PyMOL, NumPy, pandas, matplotlib, SciPy · Kafka, PostgreSQL · Kubernetes, Docker, Azure, AWS, GCP

---

[aditya.socialinfo@gmail.com](mailto:aditya.socialinfo@gmail.com)
