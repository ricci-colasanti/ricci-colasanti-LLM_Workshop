# mistral-7b‑Instruct demo

This notebook demonstrates how to:

1. **Download** the `mistral-7b-instruct-v0.2.Q4_K_M.gguf` model from Hugging Face using `requests` (streamed download, no external progress‑bar libraries required).  
2. **Load** the model with `llama_cpp.Llama`, configuring a 32 k token context and automatic thread detection.  
3. **Query** the model via `create_chat_completion` and display the response.

The workflow is self‑contained – run each cell sequentially and you’ll have a ready‑to‑use LLM inside the notebook.  

*Tip:* After the download finishes, the file remains in the notebook’s working directory, so you can reload it later without re‑downloading.





## **What is "role"?**

**Role** tells the model who is "speaking" in the conversation. Think of it like tags in a script:

### **The 3 Main Roles:**

| Role              | Meaning                                   | Example                                                      |
| ----------------- | ----------------------------------------- | ------------------------------------------------------------ |
| **`"user"`**      | **You** - the human asking questions      | `{"role": "user", "content": "What is Python?"}`             |
| **`"assistant"`** | **The AI** - the model's responses        | `{"role": "assistant", "content": "Python is a programming language..."}` |
| **`"system"`**    | **Instructions** - sets the AI's behavior | `{"role": "system", "content": "You are a helpful coding expert"}` |

## **Examples of Each Role**

### **Just user (what you're doing):**
```python
messages = [
    {"role": "user", "content": "Tell me a joke"}
]
```

### **System + user (setting personality):**
```python
messages = [
    {"role": "system", "content": "You are a pirate who speaks in pirate slang"},
    {"role": "user", "content": "Tell me a joke"}
]
# Response will be in pirate speak!
```

S
