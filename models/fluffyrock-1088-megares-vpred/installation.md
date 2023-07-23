# Installation

### Installation Info

Unlike typical Stable Diffusion 1.5 models, a few extra steps are required for the proper installation and usage of fluffyrock-1088-megares-vpred

Proper installation requires the three following files.

* an epoch of fluffyrock-1088-megares-vpred
* a v-prediction configuration file
* config rescale extension

This guide will be purely focused on installation for A1111. It will not include any information for other UI's. Please consult the documentation for these associated UI's for information about config rescaling.

{% hint style="info" %}
**Wait.. Why do I need the extension?**

The extension is required to use the classifier-free guidance part of the model. If you do not use the extension, you will still be able to generate images.&#x20;

However, they will be on very simplistic backgrounds or have little detail to them.
{% endhint %}

You will find the epochs for this model under the v-pred section.

{% embed url="https://huggingface.co/lodestones/furryrock-model-safetensors/tree/main/fluffyrock-1088-megares-terminal-snr-vpred" %}

You will also require a configuration file for the model, which can be found here.

{% embed url="https://huggingface.co/lodestones/furryrock-model-safetensors/blob/main/fluffyrock-1088-megares-terminal-snr-vpred/fluffyrock-576-704-832-960-1088-lion-low-lr-e88-terminal-snr-vpred-e61.yaml" %}

Finally, you will need the config rescale extension.

{% @github-files/github-code-block url="https://github.com/Seshelle/CFG_Rescale_webui" %}

### Guide

#### Step 1.

You will need to move the epoch for the v-prediction model into your Stable-diffusion folder of the Automatic1111 WebUI.

This can be found at the main install folder of your WebUI in the following location. With `root` being your main install location.

`root/models/Stable-diffusion`

In this example, I will be using `fluffyrock-576-704-832-960-1088-lion-low-lr-e94-terminal-snr-vpred-e67.safetensors`

You may have a newer version of the model, as indicated by the number next to `e[]` with the higher the number, the further baked the model is. Please see \[PLACEHOLDER] here for more information.

Simply place the epoch that you have into the folder indicated.

#### Step 2.

You will now need to use the download the .yaml file. This can be done by clicking onto the Hugging Face configuration file link above. You should then right-click on `raw` and then `Save Link As...` then. You should save it in the same folder as where you have placed your model epoch.

You will now be required to rename the yaml file. It needs to be renamed to the same name as your epoch.

{% hint style="info" %}
**Do I need to download this YAML every time?**

No, you do not need to continously redownload this YAML file. You can simply copy and rename it to a new epoch that you have downloaded. Provided that the model supports v-prediction, it will work fine.
{% endhint %}

For instance, if your model name is.

`fluffyrock-576-704-832-960-1088-lion-low-lr-e94-terminal-snr-vpred-e67.safetensors`

You should rename your yaml to

`fluffyrock-576-704-832-960-1088-lion-low-lr-e94-terminal-snr-vpred-e67.yaml`

Your final result should look like this.

![](<../../.gitbook/assets/CleanShot 2023-07-24 at 01.04.29@2x.png>)

Once you have completed this. Your WebUI will now know to load the model in v-prediction.

#### Step 3.

For proper usage of the model. It is strongly recommended to install the config rescale extension.

You can find this at the link below.

{% embed url="https://github.com/Seshelle/CFG_Rescale_webui" %}

To install this extension, you will need to open your WebUI.

Then, you should go to the `Extensions` tab in the UI.

After this, you should click `Manual Install` and then enter the link of the repository provided above into the `Extension GIT Repository URL` input field.

Then, simply click `Install` and wait for installation to complete. After this, restart your WebUI.
