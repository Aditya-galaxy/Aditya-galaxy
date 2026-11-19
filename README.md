## Aditya Kumar

Software Engineer and Researcher. I build systems that act on evidence, and I care most about measuring whether they are right.

---

### Research

**[openvitals](https://github.com/Aditya-galaxy/openvitals)**: open, validated sleep and recovery algorithms for wrist wearables, and a benchmark that keeps them honest.
A heart-rate-only ensemble (5 TCNs + 5 GRUs, a 1 MB ONNX file) stages sleep at kappa 0.51 on a cohort it never saw, near commercial-watch level, and `openvitals stage` runs it on Apple Health, Gadgetbridge or CSV exports. On 100 sleep-clinic patients with a different wristband, the same model halves to 0.24: the benchmark's main finding is that headline accuracy doesn't transfer across people and devices. Wrist HRV against ECG has a 16% nightly error and ranks people well, but reads about 28% high, so it's reported as a personal trend, not an absolute value.

**[nuclei-shift](https://github.com/Aditya-galaxy/nuclei-shift)**: does a cell segmentation model know when a microscope image is unlike its training data?
Cellpose's nucleus model scores zero on stained tissue and brightfield images, and inverting brightness recovers most of it. Its confidence flags its own failures almost perfectly, while the generalist model stays confident while failing. Fine-tuning on up to 50 annotated images did not catch up with the one-line fix. Also run as a Cloud Run batch job: $0.65 per 1,000 images.

**[gb1-fitness](https://github.com/Aditya-galaxy/gb1-fitness)**: can a model trained on simple protein variants predict complex ones, and does it know when it is wrong?
On the GB1 fitness landscape, neural networks beat an additive model only when training data already contains combinations of mutations, and their ensemble uncertainty carries no signal when they have to extrapolate. Protein language model features (ESM-2) lift the hardest case from 0.55 to 0.75, but a BLOSUM62 control shows half of that is amino-acid similarity alone.

#### Built and shipped

- **[noscam](https://github.com/Aditya-galaxy/noscam)**: Antivirus for scams. 2nd place, TLN Cybersecurity Challenge 2026.
- **[recap](https://github.com/Aditya-galaxy/recap)**: Screen recorder for Mac, Windows and Linux. Turns recordings into ready-to-post videos.

#### Work

Software Development Engineer Intern at **Matter** (2026): Built a distributed event streaming system in Rust and Python, peaking above 60K TPS. Contributed to backend product development and auth service, Java spring boot.

#### Tools

Python, Rust, C++, Java, SQL · PyTorch, NumPy, pandas, matplotlib, SciPy · Kafka, PostgreSQL · Kubernetes, Docker, Azure, AWS, GCP

---

[aditya.socialinfo@gmail.com](mailto:aditya.socialinfo@gmail.com)
