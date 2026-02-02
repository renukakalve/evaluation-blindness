# evaluation-blindness

📊 Evaluation Blindness in Vision Models:
Exposing robustness failures under distribution shift
High benchmark accuracy does not guarantee real-world reliability.

🔍 Overview:
This repository investigates evaluation blindness in deep vision models — the phenomenon where models achieve strong performance on standard benchmarks but fail catastrophically under small, realistic distribution shifts.

Using CIFAR-10 and CIFAR-10-C, we demonstrate that models trained and evaluated under clean conditions can appear reliable while relying on fragile shortcut features.

❓ Research Question:
Does high accuracy on clean benchmarks (e.g., CIFAR-10) reliably indicate robustness under realistic corruptions such as noise or blur?

🧪 Experimental Setup:
Dataset:
1) CIFAR-10 (clean benchmark)
2)CIFAR-10-C (corrupted benchmark)
  *Corruption used: Gaussian Noise
  *Labels unchanged (same task)

Model:
1) Architecture: ResNet-18
2) Training: from scratch
3) Loss: Cross-Entropy
4) Optimizer: SGD (standard settings)

Evaluation Protocol:
1) Train on CIFAR-10
2) Evaluate on:
  *CIFAR-10 (clean test set)
  *CIFAR-10-C (corrupted inputs)
3) No retraining or fine-tuning on corrupted data

📊 Key Results:
Dataset	Accuracy
CIFAR-10 (clean)	46.67%
CIFAR-10-C (Gaussian Noise)	10.0%

Accuracy on CIFAR-10-C drops to random-guessing level despite reasonable clean-data performance.

🧠 Key Insight
This experiment shows that standard benchmark evaluation fails to detect robustness failures.
The model relies on fragile, surface-level features that break under noise, even though benchmark accuracy suggests reasonable performance.

Conclusion:
Clean benchmark accuracy alone provides a misleading sense of real-world reliability.

📁 Repository Structure

evaluation-blindness/
├── experiments/
│   ├── CIFAR-10.py        # CIFAR-10 training
│   └── CIFAR-10-C.py     # CIFAR-10-C evaluation
├── notes/
│   ├── notes_day1.md            # Problem understanding
│   ├── notes_day2.md            # Baseline training observations
│   ├── notes_day3.md            # Failure analysis
│   └── summary.md               # Research narrative
├── data_CIFAR-10-C/
│                                # Corrupted dataset files
├── plots/                       # (Optional) result visualizations
└── README.md

▶️ How to Run
1. Train baseline model
python experiments/CIFAR-10.py

2. Evaluate on CIFAR-10-C
python experiments/CIFAR-10-C.py

📝Notes & Documentation

Detailed reasoning, predictions, and interpretations are documented in:

1) notes/notes_day1.md — Problem & hypothesis
2) notes/notes_day2.md — Baseline behavior
3) notes/notes_day3.md — Failure observation
4) notes/summary.md — Consolidated research narrative

🚧 Limitations:
*Only one corruption type evaluated
*No robustness training or mitigation applied
*Results focused on failure exposure, not solution

🔭 Future Work:
*Evaluate additional corruption types (blur, brightness)
*Analyze model confidence under corruption
*Compare with robustness-trained models
*Extend analysis to other architectures

👩‍🔬 Author

Name: [Renuka Kalve]
Background: Undergraduate researcher (AI / ML)
Interest: Robustness, evaluation failure modes, trustworthy AI

📧 [email: renukakalve777@gmail.com]
🔗 [LinkedIn: https://www.linkedin.com/in/renuka-kalve-97502a31a/ ]
