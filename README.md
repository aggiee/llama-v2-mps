# Llama 2 fork for running inference on Mac M1/M2 (MPS) devices

This is a fork of https://github.com/facebookresearch/llama that runs on Apple M2 (MPS - Metal Performance Shaders).

Please refer to the official installation, licences and usage instructions on the facebookresearch/llama page.

One workaround for unsupported 'aten:polar.out' operator is to use PYTORCH_ENABLE_MPS_FALLBACK=1 env variable.

<img width="826" alt="Llama example on M2" src="https://github.com/aggiee/llama-v2-mps/assets/9796449/f39a49da-6b74-4e8b-a734-7c6455b451eb">
