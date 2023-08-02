---
description: Basic information about the model and discoveries surrounding it.
---

# Information

## Synopsis

fluffyrock-1088-megares-vpred is a model that aims to resolve some of the design flaws of the original base model. These techniques have been shown to improve overall prompting ability, whilst improving dynamic range and contrast.

Some of the issues from Stable Diffusion 1.5, such as an inability to have very bright or very dark images have been resolved, as the vpred model has excellent capabilities in producing your prompts in any lighting.

A side effect of the modifications made to the model is that prompts appear to be much more responsive, this has several benefits but can also result in making it difficult to prompt, as the model appears to extremely precise to what you prompt and what it provides, providing no extra details unless you explicitly prompt for it.

This quirk can be incredibly powerful but some users may become frustrated from inability to prompt. For those who are newer to Stable Diffusion, we recommend using [fluffyrock-1088-megares-tsr.md](../fluffyrock-1088-megares-tsr.md "mention") instead, which uses traditional techniques with a patch to improve dynamic range capabilities.

## Technical Information

fluffyrock-1088-megares-vpred is an experimental model that uses v-prediction to fix Stable Diffusions 1.5 poor noise scheduling and sample steps. It does this in four different ways.

* By rescaling the noise schedule to enforce zero terminal SNR.
* Training the model with v-prediction
* Changing the sampler to always start from the last timestep
* Rescaling classifier-free guidance to prevent over-exposure (CFG Rescale)

These modifications have been based upon the paper "Common Diffusion Noise Schedules and Sample Steps are Flawed" which can be found here.

{% embed url="https://doi.org/10.48550/arXiv.2305.08891" %}

## Discoveries

Experimentation with the model has showed a variety of possible improvements, including but not excluded to.

* Improved understanding of prompts
* More accurate colours
* Significantly enhanced contrast

We encourage our users to experiment with our models and report feedback on them. Your feedback is what helps us to fine-tune and improve our models.

