# AceGPT-v2: Alignment at Pre-training! Towards Native Alignment for Arabic LLMs

# ✨ Latest News
* Our paper was accepted as a poster at NeurIPS 2024! (2024.10.09)
* Released alignment data on Hugging Face. (2024.08.05)
* Released AceGPT-v2 models on Hugging Face. (2024.06.17)

# ⚡ Introduction

Welcome to the AceGPT-v2 repository!

AceGPT-v2 has achieved top performance among open-source Arabic language models, excelling in benchmark tests such as `Arabic MMLU`, `EXAMS`, `AraTrust`, and `Arabic Cultural & Value Alignment`.

This repository includes:
* **Benchmark Datasets**: `Arabic-BeaverTails`, a collection of datasets we processed for benchmark testing.
* **Trained Models**: Our trained models, including base models—AceGPT-v2-8B, AceGPT-v2-32B, AceGPT-c2-70B—and chat models—AceGPT-v2-8B-chat, AceGPT-v2-32B-chat, AceGPT-v2-70B-chat.
* **Processed Alignment Data**: This includes (1) seed rewriting data annotated by the Alignment Expert (GPT-4), and (2) 10 billion tokens of Arabic alignment data processed by the Alignment Worker (a fine-tuned Qwen-1.5-4B-Chat model).

# 💭 Overview
In this paper, we introduce AceGPT-v2, a series of open-source Large Language Models (LLMs) specifically designed for the Arabic language. Building on previous work in Arabic LLM development, AceGPT-v2 focuses on aligning with human preferences during the pre-training phase—a departure from traditional post-training alignment methods. We propose a data augmentation pipeline that enhances pre-training data in key areas such as formatting, value representation, content moderation, and knowledge preservation. Through practical experiments on Arabic, followed by ablation studies, we demonstrate the feasibility and future potential of alignment during pre-training.

# 📚Data
## Benchmark Datasets
* We released benchmark datasets in [Ar-BeaverTails-Evaluation](https://huggingface.co/datasets/FreedomIntelligence/Ar-BeaverTails-Evaluation)
* The original version benchmark can be accessed at [BeaverTails-Evaluation](https://huggingface.co/datasets/PKU-Alignment/BeaverTails-Evaluation)

## Alignment Seed Data
* Seed rewriting data annotated by the Alignment Expert (GPT-4): [AceGPT-v2-AlignmentData-Seed](https://huggingface.co/datasets/FreedomIntelligence/AceGPT-v2-AlignmentData/blob/main/rewrite_seed_data.json)
* Arabic alignment data processed by the Alignment Worker (Qwen-1.5-4B-Chat): [AceGPT-v2-AlignmentData](https://huggingface.co/datasets/FreedomIntelligence/AceGPT-v2-AlignmentData)


# 👨‍⚕️ Model

## Model Access
| Model                | Backbone      | Link                                                                          |
|----------------------|---------------|-------------------------------------------------------------------------------|
| AceGPT-v2-8B | LlaMA3-8B | [Model_Weigths](https://huggingface.co/FreedomIntelligence/AceGPT-v2-8B) |
| AceGPT-v2-8B-Chat | AceGPT-v2-8B | [Model_Weigths](https://huggingface.co/FreedomIntelligence/AceGPT-v2-8B-Chat) |
| AceGPT-v2-32B | Qwen1.5-32B | [Model_Weigths](https://huggingface.co/FreedomIntelligence/AceGPT-v2-32B) |
| AceGPT-v2-32B-Chat | AceGPT-v2-32B | [Model_Weigths](https://huggingface.co/FreedomIntelligence/AceGPT-v2-32B-Chat) |
| AceGPT-v2-70B | LlaMA3-70B | [Model_Weigths](https://huggingface.co/FreedomIntelligence/AceGPT-v2-70B) |
| AceGPT-v2-70B-Chat | AceGPT-v2-70B | [Model_Weigths](https://huggingface.co/FreedomIntelligence/AceGPT-v2-70B-Chat) |



# 🤖 Limitations
Our model is primarily designed and trained to function as an AI assistant tailored for Arabic speakers. This specific design focus means that while it is optimized for generating responses to queries in Arabic, it may not produce satisfactory results for queries in other languages. Furthermore, while we have made significant advancements in the model's capabilities, it is essential to recognize its potential pitfalls. These include possible misuse, such as mishandling sensitive information, producing harmful content, perpetuating misinformation, or failing safety checks. We have not conducted an exhaustive safety check on the model, so users should exercise caution. We cannot overemphasize the need for responsible and judicious use of our model. Moreover, our evaluations predominantly relied on open-source data and the data we crafted. To achieve a more robust and comprehensive assessment, and to bolster the credibility of our findings, constructing an expansive evaluation set is imperative.

# 😀 Acknowledgement

We are aware that our works are inspired by the following works, including but not limited to

- AceGPT: https://github.com/FreedomIntelligence/AceGPT
- LLMZoo: https://github.com/FreedomIntelligence/LLMZoo
- LLaMA-Factory：https://github.com/hiyouga/LLaMA-Factory
  
Without these, nothing could happen in this repository.


# Citation
```
@inproceedings{liang2024alignment,
  title={Alignment at Pre-training! Towards Native Alignment for Arabic {LLM}s},
  author={Juhao Liang and Zhenyang Cai and Jianqing Zhu and Huang Huang and Kewei Zong and Bang An and Mosen Alharthi and Juncai He and Lian Zhang and Haizhou Li and Benyou Wang and Jinchao Xu},
  booktitle={The Thirty-eighth Annual Conference on Neural Information Processing Systems},
  year={2024},
  url={https://openreview.net/forum?id=woRFmNJiLp}
}
```
We are from the King Abdullah University of Science and Technology (KAUST), the Chinese University of Hong Kong, Shenzhen (CUHKSZ) and the Shenzhen Research Institute of Big Data (SRIBD).
