## Aditya Kumar

Software Engineer and Researcher. I build systems that act on evidence, and I care most about measuring whether they are right.

---

### Research

**[gb1-fitness](https://github.com/Aditya-galaxy/gb1-fitness)**: can a model trained on simple protein variants predict complex ones, and does it know when it is wrong?
On the GB1 fitness landscape, neural networks beat an additive model only when training data already contains combinations of mutations, and their ensemble uncertainty carries no signal when they have to extrapolate. Protein language model features (ESM-2) lift the hardest case from 0.55 to 0.75 (a BLOSUM62 control shows half of that is amino-acid similarity alone). Replaying an active learning campaign over the measured library, model-guided selection finds about 30 to 38 top-1% variants in 240 assays against 4 for random screening, and Expected Improvement reaches the best variant in 4 of 5 seeds.

**[epigenetic-clock](https://github.com/Aditya-galaxy/epigenetic-clock)**: why do epigenetic clocks trained on adult blood fail on independent cohorts?
On 656 Hannum whole-blood 450K methylation profiles (GSE40279), an ElasticNet clock (454 selected CpGs) reaches 10-fold CV MAE of 5.21 yrs ($r = 0.892$). On an independent test cohort of 89 donors (GSE41169), the model shows a $+5.95\text{ yr}$ systematic overprediction, which looks like a cross-lab transfer failure. But stratifying by age reveals an age-distribution artifact: only 35 of 656 training donors were under 40 (mean 64 yrs), while 75 of 89 test donors were under 40 (mean 31 yrs). For donors under 40, within-cohort CV bias is $+6.67\text{ yrs}$ and independent test bias is $+6.46\text{ yrs}$: young donors simply regress toward the training mean. Correlation transfers ($r = 0.920$); calibration does not.

**[protein-binder-design](https://github.com/Aditya-galaxy/protein-binder-design)**: what does a graph neural network learn first when trained on protein crystal backbones?
Trained an autoregressive ProteinMPNN graph transformer ($d_{\text{model}} = 128, k = 24$) from scratch on 29 high-resolution ($\le 2.0\text{ \AA}$) X-ray crystal structures (4,087 residues) and evaluated on 7 held-out test backbones (850 residues). In 40 epochs, test perplexity drops from 39.38 to 9.98, and native sequence recovery reaches 29.2% (against 5.0% random and 8.9% frequency baseline). Conformational pivots (Gly/Pro) learn first, reaching 70.9% recovery because turn dihedral angles geometrically demand Gly or Pro, while hydrophobic core packing reaches 25.7%. The model powers a de novo mini-protein pipeline targeting Human PD-L1 (PDB: 4ZQK).

**[threat-state-decoding](https://github.com/Aditya-galaxy/threat-state-decoding)**: can freezing and flight be decoded from prefrontal calcium activity, and does a decoder hold up on time it hasn't seen?
On 13 miniscope sessions from 7 mice during moving-threat assays, a linear decoder scores 0.886 balanced accuracy under naive random frame splits, but collapses to 0.504 when evaluated on contiguous blocks of time (chance: 0.33). The 0.382 inflation appears in all 7 mice: slow GCaMP decay and bouted behaviors leak near-identical frames across random partitions. Honest cross-validation reveals that while prefrontal activity carries genuine defensive state information above null, naive pipelines vastly overstate decoding accuracy for rare flight and freezing bouts.

**[nuclei-shift](https://github.com/Aditya-galaxy/nuclei-shift)**: does a cell segmentation model know when a microscope image is unlike its training data?
Cellpose's nucleus model scores zero on stained tissue and brightfield images, and inverting brightness recovers most of it. Its confidence flags its own failures almost perfectly, while the generalist model stays confident while failing. Fine-tuning on up to 50 annotated images did not catch up with the one-line fix. Also run as a Cloud Run batch job: $0.65 per 1,000 images.

**[openvitals](https://github.com/Aditya-galaxy/openvitals)**: open, validated sleep and recovery algorithms for wrist wearables, and a benchmark that keeps them honest.
A heart-rate-only ensemble (5 TCNs + 5 GRUs, a 1 MB ONNX file) stages sleep at kappa 0.51 on a cohort it never saw, near commercial-watch level, and `openvitals stage` runs it on Apple Health, Gadgetbridge or CSV exports. On 100 sleep-clinic patients with a different wristband, the same model halves to 0.24: the benchmark's main finding is that headline accuracy doesn't transfer across people and devices. Wrist HRV against ECG has a 16% nightly error and ranks people well, but reads about 28% high, so it's reported as a personal trend, not an absolute value.

#### Work

Software Development Engineer Intern at **Matter** (2026): Built a distributed event streaming system in Rust and Python, peaking above 60K TPS. Contributed to backend product development and auth service, Java spring boot.

#### Tools

Python, Rust, C++, Java, SQL · PyTorch, scikit-learn, Biopython, PyMOL, NumPy, pandas, matplotlib, SciPy · Kafka, PostgreSQL · Kubernetes, Docker, Azure, AWS, GCP

---

[aditya.socialinfo@gmail.com](mailto:aditya.socialinfo@gmail.com)
