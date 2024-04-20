# add_library(LLVMX86CoolPass MODULE
#   X86CoolPass.cpp)
add_llvm_pass_plugin(LLVMX86CoolPass
  X86CoolPass.cpp   
  DEPENDS
  intrinsics_gen
  X86
  BUILDTREE_ONLY)
set(LLVM_TEST_DEPENDS LLVMX86CoolPass ${LLVM_TEST_DEPENDS} PARENT_SCOPE)