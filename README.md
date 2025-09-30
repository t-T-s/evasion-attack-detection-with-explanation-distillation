# Evasion attack detection with explanation distillation

This repository accompanies Chapter 5 of the thesis: **Attack Detection with XAI**. It presents **X-ZeroSec**, a novel adversarial detection framework that leverages Explainable AI (XAI) to secure 5G and beyond wireless networks against evasion attacks.

The core innovation lies in the introduction of **explanation distillation**—a method that transfers feature attributions from a lightweight adversarial detector to a secondary XAI-based model, enabling robust generalization to unseen (zero-shot) attacks.

## 📌 Key Contributions

- 🛡️ **X-ZeroSec Architecture**: A two-stage adversarial input detector that integrates SHAP-based explanation transfer with ensemble learning.
- 📶 **DL-based Beamforming Use Case**: Applied to secure mmWave D-MIMO beamforming in 5G using DeepMIMO datasets and adversarial ML.
- 💥 **Zero-Day Attack Detection**: Robust to both white-box and black-box attacks including FGSM, PGD, CWL2, UAP, etc.
- 🧠 **Explanation Distillation**: Enhances generalization by transforming input features into explanation space (SHAP values).
- 📊 **Benchmarking**: Compared against state-of-the-art defences like MagNet, adversarial training (Madry, TRADES), and naive Bayes classifiers.
- 🧪 **Experimental Validation**: Tested across simulation and a real O-RAN testbed with latency profiling and robustness analysis.
- 🌐 **Extension to DDoS Detection**: Demonstrated generalizability to SDN-based volumetric DDoS attacks using FFT-transformed traffic patterns.

## 🧰 Components

- `src/`: Code for training beamforming prediction models, adversarial detectors, and explanation distillation classifiers.
- `notebooks/`: Interactive Jupyter notebooks for attack generation, SHAP visualizations, and evaluation plots.
- `oran/`: Scripts and configs for OAI/O-RAN testbed deployment and telemetry.
- `ddos/`: DDoS detection pipeline using FFT + XAI with SDN emulation (Mininet + GNS3).
- `results/`: Figures and logs for detection accuracy, latency benchmarks, and attack robustness.

## 🧠 Technologies Used

- Python (NumPy, SciKit-Learn, XGBoost, SHAP)
- TensorFlow/Keras (Beamforming NN model)
- DeepMIMO dataset
- OAI RAN + O-RAN xApps (Testbed)
- SHAP (TreeSHAP for explanation generation)

## 📈 Performance Highlights

- ✅ **Detection Accuracy (Seen Attacks)**: 96%–99%
- 🔍 **Zero-Shot Detection Accuracy**: Up to 96% (XAI model)
- 🧪 **Black-box Attack Recall**: >92% (XAI) vs <84% (Direct)
- ⚡ **End-to-End Latency**: 3.5 ms per prediction (CPU); within URLLC thresholds
- 🧱 **Scalability**: Achievable rate maintained despite high adversarial load

## 📄 Citation

If you use this code or data in your research, please cite:

