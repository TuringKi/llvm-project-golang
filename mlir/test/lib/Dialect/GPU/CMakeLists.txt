# Exclude tests from libMLIR.so
add_mlir_library(MLIRGPUTestPasses
  TestConvertGPUKernelToCubin.cpp
  TestConvertGPUKernelToHsaco.cpp
  TestGpuMemoryPromotion.cpp
  TestGpuParallelLoopMapping.cpp
  TestGpuRewrite.cpp

  EXCLUDE_FROM_LIBMLIR

  LINK_LIBS PUBLIC
  MLIRAffine
  MLIRGPUOps
  MLIRGPUToGPURuntimeTransforms
  MLIRLLVMToLLVMIRTranslation
  MLIRNVVMIR
  MLIRNVVMToLLVMIRTranslation
  MLIRPass
  MLIRROCDLIR
  MLIRROCDLToLLVMIRTranslation
  MLIRSCF
  MLIRStandard
  MLIRTransformUtils
  )
