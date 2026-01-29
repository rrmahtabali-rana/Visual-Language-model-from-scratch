# Visual-Language-model-from-scratch
Nano CLIP-style vision–language from scratch on synthetic geometric shapes (PyTorch).

This repo contains a tiny **CLIP-style vision–language alignment** experiment trained **from scratch** on a fully synthetic dataset of geometric shapes.

It is intentionally small and easy to understand:
- Synthetic images: colored **square / circle / triangle** at different **positions**
- Text captions: `"<color> <shape> <position>"` (e.g., `"red circle top-left"`)
- Two encoders (image + text) produce embeddings that are aligned with a CLIP-like contrastive loss.

> Note: this is **not** a large-scale, generative VLM (it does not generate free-form text).  
> It’s a **nano** example of *vision–language alignment / retrieval* for learning and debugging.

---

## What’s inside

- `Nano VLM_from_scratch.ipynb`  
  End-to-end notebook:
  1. Build synthetic dataset (243 samples)
  2. Train/val split (80/20)
  3. Image encoder (small CNN → embedding)
  4. Text encoder (token + positional embeddings + multi-head attention → `[CLS]`)
  5. CLIP-like contrastive loss
  6. Retrieval demo (image→text and text→image)

---

## Quick start (Colab)

1. Upload the notebook to Colab (or open it from GitHub).
2. Run cells top to bottom.

---

## Run locally

### Install
```bash
pip install -r requirements.txt
