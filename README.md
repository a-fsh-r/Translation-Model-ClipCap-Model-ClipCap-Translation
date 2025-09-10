# 🌍 Image Captioning & Translation Pipeline

This repository explores the intersection of vision and language using three different model setups. The goal is to not only generate captions for images but also make them accessible to Farsi (Persian) speakers through translation.

# 🔹 Model 1: Translation-Model

This model focuses only on text translation.

Input: English sentence

Output: Farsi sentence

Powered by SeamlessM4T, which supports multilingual translation.

- Example:

EN: “A dog is playing with a ball.”

FA: “سگی در حال بازی با توپ است.”

# 🔹 Model 2: ClipCap-Model

This model handles image captioning in English.

Input: Image

Output: English caption

Based on ClipCap (CLIP + GPT-2).

- Example:

Input image → “A man riding a horse on the beach.”

# 🔹 Model 3: ClipCap-Translation

This is the full pipeline, combining the previous two.

Step 1: Generate caption in English with ClipCap.

Step 2: Translate caption into Farsi with SeamlessM4T.

Output: Captions in both English and Farsi.

- Example:

Input image → EN: “A man riding a horse on the beach.”

Output → FA: “یک مرد در حال سوارکاری در ساحل است.”

# ✨ Together, these three models demonstrate how we can:

Caption images in English.

Translate English text into Farsi.

Build a seamless pipeline from image → English caption → Farsi caption.

# 🧩 Code Overview

The repository is organized into three main components, reflecting the three model setups (Translation, ClipCap, ClipCap-Translation).

# 📂 notebooks/ – Usage Examples

- Translation-Model:

Demonstrates how to translate English sentences into Farsi.

- ClipCap-Model:

Shows how to load images, extract features, and generate captions in English.

- ClipCap-Translation:

Full pipeline: image → English caption → Farsi translation.

# 📂 images/ & annotations/

Store COCO dataset images (e.g., val2014) and captions annotations.

Used for both captioning and evaluation.

# 📄 requirements.txt

Lists all dependencies (PyTorch, HuggingFace Transformers, OpenAI CLIP, etc.).

# 📄 model_weights.pt

Pretrained weights for the ClipCap projection model.

# ⚡ With this structure:

You can run notebook to test translation only, captioning only, or the combined pipeline.
