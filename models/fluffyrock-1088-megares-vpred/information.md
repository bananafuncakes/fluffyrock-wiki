---
description: Basic information about the model and discoveries surrounding it.
---

# Information

## Synopsis

fluffyrock-1088-megares-vpred is an experimental model that uses v-prediction to fix Stable Diffusions 1.5 poor noise scheduling and sample steps. It does this in four different ways.

* By rescaling the noise schedule to enforce zero terminal SNR.
* Training the model with v-prediction
* Changing the sampler to always start from the last timestep
* Rescaling classifier-free guidance to prevent over-exposure (config rescale)

These modifications have been based upon the paper "Common Diffusion Noise Schedules and Sample Steps are Flawed" which can be found here.

{% embed url="https://doi.org/10.48550/arXiv.2305.08891" %}

## Discoveries

Experimentation with the model has showed a variety of possible improvements, including but not excluded to.

* Improved understanding of prompts
* More accurate colours
* Significantly enhanced contrast

We encourage our users to experiment with our models and report feedback on them. Your feedback is what helps us to fine-tune and improve our models.

