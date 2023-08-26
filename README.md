# Training and Fine-Tuning CLIP Models

## Description
| ![CLIP](https://raw.githubusercontent.com/mlfoundations/open_clip/main/docs/CLIP.png) |
|:--:|
| Image Credit: https://github.com/openai/CLIP |

This project trains and fine-tunes CLIP models on custom datasets.

CLIP (Contrastive Language-Image Pre-training) is a vision-language model introduced by OpenAI that shows strong performance on downstream tasks through zero-shot transfer. 

In this project, we start from pretrained CLIP models and fine-tune them on our own datasets to adapt the models to new domains and tasks.

## Models

We use the following CLIP models from the [official repository](https://github.com/openai/CLIP):

- CLIP ViT-B/32
- CLIP ViT-B/16 
- CLIP ViT-L/14

These models provide a good selection of model sizes and capacities.

## Training Process 

CLIP is trained on image-text pairs in a contrastive manner. Therefore, our dataset needs to contain (image, text) pairs suitable for the domain.  

The models are first pretrained on a large generic dataset, then fine-tuned on our target dataset. 

Training code adapts the official CLIP training scripts for our datasets.

## Evaluation

Fine-tuned CLIP models are evaluated on downstream tasks like:

- Image-text retrieval
- Image classification
- Text-to-image generation

Zero-shot capabilities are also analyzed.

## Datasets

We use the following datasets:

- Generic large-scale dataset for pretraining (e.g. YFCC15M)
- Our own domain-specific dataset for fine-tuning (e.g. medical images and reports)

## References 

- [CLIP](https://arxiv.org/abs/2103.00020)
- [OpenAI CLIP](https://github.com/openai/CLIP)
