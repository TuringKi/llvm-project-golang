add_mlir_dialect_library(MLIRMath
  MathOps.cpp
  MathDialect.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir/Dialect/Math

  DEPENDS
  MLIRMathOpsIncGen

  LINK_LIBS PUBLIC
  MLIRArithmetic
  MLIRDialect
  MLIRIR
  )
