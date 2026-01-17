# UCRNLP Screening (Fall ’26) — More Effort Route Submission

This repository contains my submission materials for Prof. Yue Dong’s UCR NLP Lab screening (“More Effort Route”), completing the **AI Safety** option: **multi-modal adversarial attacks / CLIP embedding optimization** using the official project **Jailbreak in Pieces** (ICLR 2024).

- Official repo: https://github.com/erfanshayegani/Jailbreak-In-Pieces  
- Paper (arXiv): https://arxiv.org/abs/2307.14539  

## What’s included
- **Colab notebook (.ipynb):** full runnable code used to generate all results.
- **Report (PDF):** 2–4 page analysis report with exact tables/figures referenced.

## Experiment design (benign images only)
Safety constraint: **No harmful/NSFW prompts or content.** Targets are benign images only (checkerboard, nature, solid gray, circles, white).

1) **Baseline:** CLIP cosine similarity analysis on **5 benign samples** (+ heatmap).  
2) **Attack Run 1:** CLIP embedding optimization from **white init** to each benign target using  
   - `epochs = 800`, `lr = 0.05`, `seed = 42`  
3) **Attack Run 2 (Ablation):** change exactly **one** knob:  
   - `epochs = 300` (keep `lr = 0.05`, `seed = 42`, init/model the same)  
4) **Failure case:** hardest target by `final_loss` (default: **circles**).

## Environment
- GPU: **Tesla T4 (Colab)**
- Python: **3.12.12**
- torch: **2.9.0+cu126** (CUDA enabled)
- torchvision: **0.24.0+cu126**
- transformers: **4.57.3**
- CLIP: **openai/clip-vit-large-patch14-336**

## Files
- Notebook: `UCRNLP_JailbreakInPieces_Attack.ipynb`
- Report: `UCRNLP_JailbreakInPieces_Report.pdf`

## Notes
This work is for a research skills screening task. All analyses are conducted independently, while using the official repo/paper as the base reference.

## Author
SK Rakib Ul Islam Rahat  
Google Scholar: https://scholar.google.com/citations?user=0X1eRi8AAAAJ&hl=en  
GitHub: https://github.com/skrakibulislamrahat
