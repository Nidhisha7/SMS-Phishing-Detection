# SMS Phishing Detection

The model detects whether an SMS message is safe or a phishing attempt, and if phishing is detected, further classifies the attack type as phone-based, URL-based, or email-based. The system is built on DistilBERT and optimised for lightweight on-device mobile deployment.

---

## Model Architecture

The framework follows a two-stage cascaded classification approach:

- **Stage 1:** Binary classification — Safe or Phishing
- **Stage 2:** Attack type classification — Phone, URL, or Email phishing (activated only when Stage 1 detects phishing)

---

## Training Results

![Training History](https://github.com/user-attachments/assets/b41f1428-c81b-46a8-a2ec-43dc419315c6)

---

## Dataset

The model was trained on a combined dataset of approximately 9,300 SMS messages sourced from:

- Mendeley SMS Phishing Collection - Mishra and Soni (2022)
- SmishTank - Timko and Rahman (2024)

---


## Requirements

- Python 3.8+
- PyTorch
- Transformers (HuggingFace)
- Android Studio (for app deployment)

---

## Results

| Metric | Score |
|--------|-------|
| Stage 1 Accuracy | ~99% |
| Stage 2 Accuracy | ~95% |
| Combined F1 Score | ~0.97 |
