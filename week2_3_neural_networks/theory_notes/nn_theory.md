# Neural Networks — Theory Notes
**SoC 2026 | Week 2–3**

---

## 1. What is a Neural Network?

A neural network is a **function approximator** made of layers of interconnected nodes (neurons). Each neuron computes:

```
output = activation( W · input + b )
```

Where `W` are weights, `b` is a bias, and `activation` is a non-linear function.

---

## 2. Key Components

| Component | Role |
|---|---|
| **Weights W** | Learned parameters — control signal strength |
| **Bias b** | Shifts the activation threshold |
| **Activation fn** | Introduces non-linearity (without it, the network is just linear regression) |
| **Loss function** | Measures how wrong the prediction is |
| **Optimiser** | Updates W and b to reduce loss |

---

## 3. Activation Functions

| Function | Formula | Use case |
|---|---|---|
| Sigmoid | `1 / (1 + e^-z)` | Binary output layer |
| ReLU | `max(0, z)` | Hidden layers (default) |
| Tanh | `(e^z - e^-z) / (e^z + e^-z)` | Centred hidden layers |
| Softmax | `e^zi / Σ e^zj` | Multi-class output |

---

## 4. Forward Propagation

Data flows **forward** through the network, layer by layer:

```
Z[l] = W[l] · A[l-1] + b[l]
A[l] = activation(Z[l])
```

The final layer outputs a **prediction** `ŷ`.

---

## 5. Loss Functions

- **Binary Cross-Entropy** (binary classification):
  ```
  L = -1/m Σ [ y·log(ŷ) + (1-y)·log(1-ŷ) ]
  ```
- **Categorical Cross-Entropy** (multi-class):
  ```
  L = -1/m Σ Σ y_ij · log(ŷ_ij)
  ```
- **MSE** (regression):
  ```
  L = 1/m Σ (y - ŷ)²
  ```

---

## 6. Backpropagation

Backprop computes **gradients of the loss** w.r.t. every weight using the **chain rule**:

```
dL/dW[l] = dL/dA[l] · dA[l]/dZ[l] · dZ[l]/dW[l]
```

Going backwards, layer by layer.

---

## 7. Gradient Descent

Once we have gradients, we update parameters:

```
W := W - α · dL/dW
b := b - α · dL/db
```

where `α` is the **learning rate** (controls step size).

### Variants

| Variant | Batch size | Notes |
|---|---|---|
| Batch GD | All data | Slow, stable |
| Stochastic GD | 1 sample | Fast, noisy |
| Mini-batch GD | 32–256 | Best of both |

---

## 8. Overfitting & Regularisation

- **Overfitting**: model memorises training data, fails on unseen data
- **Solutions**:
  - L2 Regularisation: penalise large weights (`λ·||W||²`)
  - Dropout: randomly zero out neurons during training
  - Early stopping: stop when validation loss increases
  - More data / data augmentation

---

## 9. Hyperparameters

| Hyperparameter | Typical values |
|---|---|
| Learning rate | 0.001 – 0.1 |
| Hidden units | 16, 32, 64, 128, 256 |
| Batch size | 32, 64, 128 |
| Epochs | 100 – 1000 |
| Activation | ReLU (hidden), Sigmoid/Softmax (output) |

---

## 10. Resources

- [StatQuest Neural Networks (Videos 74–84)](https://www.youtube.com/watch?v=Gv9_4yMHFhI&list=PLblh5JKOoLUICTaGLRoHQDuF_7q2GfuJF)
- [Andrew Ng Course 2 — Improving Deep Neural Networks](https://www.youtube.com/watch?v=ggWLvh484hs&list=PLyoNSC4BT4eVpykPF0Yx8C1Zs50XtD17L)
