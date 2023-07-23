---
description: Important information and tips and tricks with the model.
---

# Important Notes & Tips

* Embeddings appear to have some issues and may require retraining. They seem to have a tendency to "wash out" the image.
* LoRA's appear to have varying levels of performance. You may experience unexpected behaviour whilst using them.
* There isn't a way to know about how merging will work. Inpainting merges do not appear to work. You should use the base model for merges.
* If you are experiencing significant issues with your prompt, even after removing embeddings and LoRA's. You should go through your prompt and remove any unusual prompting practices. This may include things such as extremely high emphasis for certain tags, ridiculous amounts of negatives and other older prompting techniques.
* Controlling contrast or brightness can be quite the challenge. `dark` is a very strong keyword and may be too strong on it's own. Sometimes, it will make the characters body black. A controllable way to control brightness is using negative prompts such as `white background` and `black background` adjusted with the weights to what you need. Negative prompting `simple background` helpsmore unconditionally.

