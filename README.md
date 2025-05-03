# Quen3
# 🧠 Qwen-3 0.6B Chat Inference with Hugging Face & KaggleHub

This project demonstrates how to run **inference** on the lightweight [Qwen-3 0.6B](https://huggingface.co/Qwen) large language model using **Hugging Face Transformers** and **KaggleHub**.

It uses a simple prompt to trigger both "thinking" and final answer generation by the model.

---

## 📂 Files

- `qwen_chat_inference.py` – Main Python script for running the model
- `README.md` – You're here!
- *(Optional)* `requirements.txt` – Install dependencies

---

## 📦 Installation

Make sure Python 3.8+ is installed. Then install dependencies:

```bash
pip install torch transformers kagglehub
```

---

## 🚀 Usage

Run the script with:

```bash
python qwen_chat_inference.py
```

The model will:
1. Download Qwen-3 0.6B via KaggleHub
2. Prepare a prompt (`"what is 3*4"`)
3. Enable internal reasoning (`enable_thinking=True`)
4. Generate and print the final response

---

## 🧠 Thinking Mode

The script uses:

```python
enable_thinking=True
```

This lets the model:
- Simulate internal "thoughts" before answering
- Output is split into:
  - `thinking_content` (optional)
  - `content` (final user-facing response)

---

## 🧾 Example Output

```
content: The result of 3*4 is 12.
```

You can also uncomment a line in the script to print the model's **internal reasoning**.

---

## ⚙️ Configuration

| Parameter        | Description                              |
|------------------|------------------------------------------|
| `prompt`         | Customize the input question             |
| `max_new_tokens` | Controls how much output the model generates |
| `enable_thinking`| Toggle internal reasoning mode           |

---

## 📄 License

This example uses the **Qwen-3 0.6B** model. Check [Qwen's license](https://huggingface.co/Qwen) for details on usage rights and restrictions.

---

## 🙋‍♂️ Author

Created as a minimal demo for chat-style LLM inference with Hugging Face and KaggleHub.

---

## ✅ Todo

- [ ] Add web UI using Gradio or Streamlit
- [ ] Add batch generation for multiple prompts
