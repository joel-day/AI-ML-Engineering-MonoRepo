# GPU usage Huggung Face => Optimum (w/ quantization) => ONNX => DirectML

# GPU: Radeon 6750 XT (based on the RDNA 2 architecture) 

## Limitations

Isnt compatibale with CUDA (NVIDIA ONLY)


AMD does not officially support RDNA2 GPUs (like 6750 XT) for full ROCm/HIP SDK development.

Isnt compatibale with ROCm  (AMD's GPU compute stack (like CUDA for NVIDIA))
1) doesnt support my driver(HIP SDK)
ROCm primarily supports CDNA and some GCN architectures
2) Its (Linux only).

Due to these limitations, other tools need to be used (DirectML & ONNX). Cnsequently training with DirectML & ONNX on is currently inference-only



## Features 

It can run the ROCm Runtime (ONNX runtime). use precompiled binaries that target ROCm runtime and are architecture-agnostic enough to run on RDNA2.

You can run ROCm applications (like PyTorch with AMD backend or ONNX runtime) if prebuilt for the runtime.



DirectX 12 (DirectML works with any DirectX 2 GPUS including NVIDIA but CUDA is the better option there)




## ONNX (First Release: 2017) Files:
Model Weights: The ONNX file stores model weights (like the learned parameters from training).

Computation (Forward Pass): During inference, the ONNX Runtime (or another inference engine) takes those weights and performs the forward pass (calculations) to generate predictions.

ONNX works with many popular frameworks, including TensorFlow, PyTorch, MXNet, Caffe2, and others.


PyTorch is not required at all. The model is simply loaded and run via ONNX Runtime, using DirectML as the backend for hardware acceleration.



ONNX Runtime performs inference, and DirectML (First Release: 2019) acts as a backend to optimize this inference on AMD GPUs like the Radeon 6750 XT. DirectML supports AMD GPUs with RDNA 2 architecture 