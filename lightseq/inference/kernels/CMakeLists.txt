cmake_minimum_required(VERSION 3.18)

set(cuda_kernel_files
    gptKernels.cc.cu transformerKernels.cc.cu multilgKernels.cc.cu
    embKernels.cc.cu embKernels_int8.cc.cu transformerKernels_int8.cc.cu)

add_library(cuda_kernels STATIC ${cuda_kernel_files})
target_include_directories(cuda_kernels INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
