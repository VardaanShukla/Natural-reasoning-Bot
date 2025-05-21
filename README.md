# Natural Reasoning Bot 🤖

A lightweight QA chatbot built using Hugging Face's `facebook/natural_questions` dataset and a fine-tuned `distilgpt2` model. This project provides a simple Streamlit interface to interact with the model in a clean, animated UI.

---

## ✨ Features

* Reasoning-based natural language answers
* Animated Streamlit UI with gradient layout
* Fine-tuned GPT-style language model
* Clean prompt formatting with context handling
* Ready for deployment on GitHub or Streamlit Cloud

---

## 🎓 Example Questions That Work Best

Use questions that require factual understanding, calculation, or reasoning:

| Question Example                                     | Why It Works                    |
| ---------------------------------------------------- | ------------------------------- |
| What is the total work done on an object lifted 5m?  | Physics-based factual reasoning |
| Why is work zero in circular motion?                 | Conceptual explanation          |
| If a car moves 60km/h for 2 hours, what is distance? | Simple arithmetic reasoning     |

> Avoid vague or one-word questions like "gravity" or "work".

Always format your prompt like this:

```txt
### Question: <your question>
### Answer:
```

---

## 📊 Accuracy Evaluation (Optional)

To evaluate model performance, you can measure accuracy or BLEU/ROUGE scores if using a validation dataset. Here's a simple accuracy graph generation using matplotlib:

```python
import matplotlib.pyplot as plt

# Sample accuracy values per epoch
epochs = [1, 2, 3, 4, 5]
train_acc = [0.52, 0.65, 0.72, 0.78, 0.81]
val_acc = [0.50, 0.63, 0.70, 0.75, 0.79]

plt.plot(epochs, train_acc, label='Train Accuracy', marker='o')
plt.plot(epochs, val_acc, label='Validation Accuracy', marker='x')
plt.xlabel("Epoch")
plt.ylabel("Accuracy")
plt.title("Training vs Validation Accuracy")
plt.legend()
plt.grid(True)
plt.show()
```

---

## 🚀 How to Run

1. **Install requirements**

```bash
pip install -r requirements.txt
```

2. **Run Streamlit App**

```bash
streamlit run app.py
```

---

## 🌐 Folder Structure

```
project/
├── app.py               # Streamlit UI app
├── model/               # Fine-tuned model directory
├── utils.py             # Utility functions for prompt formatting
├── requirements.txt    # Dependencies
└── README.md            # Project readme
```

---

## 💪 Credits

* Hugging Face Transformers
* Streamlit
* Dataset: `facebook/natural_questions`
* Model: `distilgpt2`

---

For deployment on GitHub/Streamlit Cloud, keep model size small and test on CPU mode.

**Made with ❤️ by \[Vardaan Shukla]**
