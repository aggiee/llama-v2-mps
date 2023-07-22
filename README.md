# Llama 2 fork for running inference on Mac M1/M2 (MPS) devices

This is a fork of https://github.com/facebookresearch/llama that runs on Apple M2 (MPS - Metal Performance Shaders).

Please refer to the official installation, licences and usage instructions on the facebookresearch/llama page.

* **Note**: user needs to **set PYTORCH_ENABLE_MPS_FALLBACK=1 env variable** to run this code.
  * This is a workaround for unsupported 'aten:polar.out' operator.
  * If you see the following message, it is expected. It falls back to CPU for that specific operation and the warning is to inform the user about it:
_"UserWarning: The operator 'aten::polar.out' is not currently supported on the MPS backend and will fall back to run on the CPU. This may have performance implications. (Triggered internally at /private/var/folders/nz/j6p8yfhx1mv_0grj5xl4650h0000gp/T/abs_1aidzjezue/croot/pytorch_1687856425340/work/aten/src/ATen/mps/MPSFallback.mm:11.)
freqs_cis = torch.polar(torch.ones_like(freqs), freqs) # complex64"_

The code should run past that as shown in this screenshot.

<img width="826" alt="Llama example on M2" src="https://github.com/aggiee/llama-v2-mps/assets/9796449/f39a49da-6b74-4e8b-a734-7c6455b451eb">
