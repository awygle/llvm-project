add_mlir_dialect_library(MLIRStandardOps
  IR/Ops.cpp
  EDSC/Builders.cpp
  EDSC/Intrinsics.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir/Dialect/StandardOps

  DEPENDS
  MLIRStandardOpsIncGen

  LINK_LIBS PUBLIC
  MLIRCallInterfaces
  MLIRControlFlowInterfaces
  MLIREDSC
  MLIRIR
  MLIRSideEffects
  MLIRViewLikeInterface
  )

add_subdirectory(Transforms)
