### Aditya Kumar

Software engineer moving into computational biology. I build systems that act on evidence, and I care most about measuring whether they are right.

**Now:** looking for research internships and PhD positions in human biology, health, neuroscience and ageing, where machine learning meets biological data.

---

#### Research

**[openvitals](https://github.com/Aditya-galaxy/openvitals)**: open, validated sleep and recovery algorithms for wrist wearables, and a benchmark that keeps them honest.
Whole-night sequence models beat standard baselines by 0.11 to 0.18 kappa, including when trained on one cohort and tested on another, and once a model sees the whole night, adding motion makes no measurable difference. Subject-wise splits, five seeds, confidence intervals that resample people rather than nights.

**[nuclei-shift](https://github.com/Aditya-galaxy/nuclei-shift)**: does a cell segmentation model know when a microscope image is unlike its training data?
Cellpose's nucleus model scores zero on stained tissue and brightfield images, and inverting brightness recovers most of it. Its confidence flags its own failures almost perfectly, while the generalist model stays confident while failing. Fine-tuning on up to 50 annotated images did not catch up with the one-line fix. Also run as a Cloud Run batch job: $0.65 per 1,000 images.

**[gb1-fitness](https://github.com/Aditya-galaxy/gb1-fitness)**: can a model trained on simple protein variants predict complex ones, and does it know when it is wrong?
On the GB1 fitness landscape, neural networks beat an additive model only when training data already contains combinations of mutations, and their ensemble uncertainty carries no signal when they have to extrapolate. Protein language model features (ESM-2) lift the hardest case from 0.55 to 0.75, but a BLOSUM62 control shows half of that is amino-acid similarity alone.

**[kronagent](https://github.com/Aditya-galaxy/kronagent)**: an AI agent for cloud security response that earns its autonomy.
Each action class runs unattended only after a measured bound on how often it would have been wrong, and is suspended after a wrong autonomous action. Includes a prompt-injection red-team suite and an evaluation harness with confidence intervals. Source-available.

**[hyperion](https://github.com/Aditya-galaxy/hyperion)**: what exchange notices do to crypto prices, second by second.
An event study of 433 Upbit notices against Binance's one-second prices: the median listing trade paid only if filled in the same second as the notice, and lost money after fees one second later.

#### Built and shipped

- **[noscam](https://github.com/Aditya-galaxy/noscam)**: holds payments, OTPs and app installs that came from a scam message, and flags hidden spyware on Android. 2nd place, TLN Cybersecurity Challenge 2026.
- **[hopscotch](https://github.com/Aditya-galaxy/hopscotch)**: an agent fleet that keeps school districts within legal deadlines for special education evaluations. Gemini and Google ADK on Cloud Run.
- **[recap](https://github.com/Aditya-galaxy/recap)**: turns screen recordings into step-by-step guides and bug reports, on your own computer.

#### Work

Software Development Engineer Intern at **Matter Link** (2026): a distributed event streaming system in Rust and Python, peaking above 60,000 messages a second.

#### Tools

Python, Rust, C++, Java, SQL · PyTorch, NumPy, pandas, SciPy · Kafka, PostgreSQL · Kubernetes, Docker, AWS, Azure, GCP

---

[aditya.socialinfo@gmail.com](mailto:aditya.socialinfo@gmail.com)
