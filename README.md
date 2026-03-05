# Meta‑Llama‑3‑8B‑Instruct demo

This notebook demonstrates how to:

1. **Download** the `Meta‑Llama‑3‑8B‑Instruct‑Q4_K_M.gguf` model from Hugging Face using `requests` (streamed download, no external progress‑bar libraries required).  
2. **Load** the model with `llama_cpp.Llama`, configuring a 32 k token context and automatic thread detection.  
3. **Query** the model via `create_chat_completion` and display the response.

The workflow is self‑contained – run each cell sequentially and you’ll have a ready‑to‑use LLM inside the notebook.  

*Tip:* After the download finishes, the file remains in the notebook’s working directory, so you can reload it later without re‑downloading.
