# 🤖 Build Your Own GPT — from Scratch
**Programme:** IIT Bombay Summer of Science (SoS) 2026
**Project:** Build Your Own GPT
**Submitted by:** Bhavya Upadhyay (Roll No. 24B2229)

---

## 📁 Repository Structure

```
soc-midterm/
├── week1_ds_tools/          # NumPy, Pandas, Matplotlib
│   ├── numpy/
│   ├── pandas/
│   └── matplotlib/
├── week2_3_neural_networks/ # Neural Network fundamentals
│   ├── theory_notes/
│   └── implementations/
├── week4_advanced_nn/       # CNNs & advanced architectures
├── resources/               # Cheatsheets, reference links
└── assets/                  # Images, plots
```

---

## 📅 Weekly Progress

### ✅ Week 1 — Essential Data Science Tools

Core Python libraries that underpin everything in this project.

| Library | Notebook | Topics Covered |
|---|---|---|
| NumPy | [`numpy_basics.ipynb`](week1_ds_tools/numpy/numpy_basics.ipynb) | Arrays, broadcasting, linear algebra ops |
| Pandas | [`pandas_basics.ipynb`](week1_ds_tools/pandas/pandas_basics.ipynb) | DataFrames, groupby, merging, time-series |
| Matplotlib | [`matplotlib_basics.ipynb`](week1_ds_tools/matplotlib/matplotlib_basics.ipynb) | Line/bar/scatter plots, subplots, styling |

**Resources used:**
- [Python in 1 Hour — Programming with Mosh](https://www.youtube.com/watch?v=kqtD5dpn9C8)
- [Intro to NumPy](https://www.youtube.com/watch?v=QUT1VHiLmmI)
- [Intro to Pandas](https://www.youtube.com/watch?v=vmEHCJofslg)
- [Matplotlib Tutorial](https://www.youtube.com/watch?v=DAQNHzOcO5A)

---

### ✅ Week 2 & 3 — Neural Networks

Building neural networks from scratch before moving to frameworks — the foundation for understanding transformers.

| Notebook | Topics Covered |
|---|---|
| [`perceptron.ipynb`](week2_3_neural_networks/implementations/perceptron.ipynb) | Perceptron, activation functions, BCE loss |
| [`neural_net_from_scratch.ipynb`](week2_3_neural_networks/implementations/neural_net_from_scratch.ipynb) | Forward pass, backprop, mini-batch GD |

**Theory notes:** [`week2_3_neural_networks/theory_notes/nn_theory.md`](week2_3_neural_networks/theory_notes/nn_theory.md)

**Resources used:**
- [StatQuest Neural Networks playlist](https://www.youtube.com/watch?v=Gv9_4yMHFhI&list=PLblh5JKOoLUICTaGLRoHQDuF_7q2GfuJF) (Videos 74–84)
- [Andrew Ng ML Specialization — Course 1](https://www.youtube.com/watch?v=vStJoetOxJg&list=PLkDaE6sCZn6FNC6YRfRQc_FbeQrF8BwGI)
- [Andrew Ng ML Specialization — Course 2](https://www.youtube.com/watch?v=ggWLvh484hs&list=PLyoNSC4BT4eVpykPF0Yx8C1Zs50XtD17L)

---

### ✅ Week 4 — Advanced Neural Networks

Convolutional networks and advanced architectures — key stepping stones toward attention and transformers.

| Notebook | Topics Covered |
|---|---|
| [`cnn_basics.ipynb`](week4_advanced_nn/cnn_basics.ipynb) | Convolutions, pooling, feature maps, CNN architecture |

**Resources used:**
- [StatQuest playlist](https://www.youtube.com/watch?v=Gv9_4yMHFhI&list=PLblh5JKOoLUICTaGLRoHQDuF_7q2GfuJF) (Videos 86–91)

---

## 🛠️ Setup & Usage

```bash
# Clone the repo
git clone https://github.com/<your-username>/soc-byog-2026.git
cd soc-byog-2026

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
```

---

## 📦 Dependencies

See [`requirements.txt`](requirements.txt). Core libraries:
- `numpy`, `pandas`, `matplotlib`
- `scikit-learn`
- `jupyter`

---

## 📌 Notes

- All notebooks are self-contained with markdown explanations alongside code.
- Code is written for clarity over performance — the goal is understanding.
- Plots are saved to [`assets/`](assets/) where relevant.
