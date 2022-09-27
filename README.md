# GPT-Models-Text-Generation
In this repo I have shared how to use smaller versions of the GPT-Neo, GPT-J and BLOOM models to generate text for a given prompt.

All these models were loaded and run in Google Colab since it gives us free access to around 12GB GPU RAM.

## [GPT-NEO](https://github.com/daparasyte/GPT-Models-Text-Generation/blob/main/GPT_Neo.ipynb)
Using Hugging Face Transformers, we can easily load the desired GPT-Neo model. However, the GPT-Neo-2.7B model requires more than 13GB GPU VRAM. 
If you have the required GPU RAM you can go ahead with this model, else you can use the GPT-Neo-1.3B model which can easily by run on Google Colab.

__NOTE__ - *The GPT-Neo model is no longer maintained, however you can check their [GitHub](https://github.com/EleutherAI/gpt-neo) for reference.*

## [GPT-J-6B](https://github.com/daparasyte/GPT-Models-Text-Generation/blob/main/gpt_j_6B_8bit.ipynb)
The original GPT-J model requires 22+GB GPU memory to just load the model (float32 parameters). The model won't fit on most single-GPU setups short of A6000 and A100.
In the code shared, we have used used something called 8-bit compression using [bitsandbytes](https://github.com/TimDettmers/bitsandbytes) library.
This allows us to load and use the model using around 8GB GPU memory without any significant difference in the performance of the model.

You can check out the original model [here](https://github.com/kingoflolz/mesh-transformer-jax)

## [BLOOM](https://github.com/daparasyte/GPT-Models-Text-Generation/blob/main/hugging_face_int8.ipynb)
We can run our own 8-bit model on any Hugging Face model (lighter versions) using the bitsandbytes library mentioned before.
This notebook is a demo of how to use BLOOM-3B model with the bistandbytes integration in Hugging Face models.
Reference - [HF bitsandbytes Integration](https://huggingface.co/blog/hf-bitsandbytes-integration)
