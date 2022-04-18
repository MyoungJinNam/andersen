include_directories (${andersen_SOURCE_DIR}/include)

add_llvm_library(Temp_Anderson MODULE
  Andersen.cpp
  AndersenAA.cpp
  ConstraintCollect.cpp
  ConstraintOptimize.cpp
  ConstraintSolving.cpp
  ExternalLibrary.cpp
  NodeFactory.cpp
 
 ADDITIONAL_HEADER_DIRS
 ../include

 DEPENDS
 intrinsics_gen
 
 #COMPONENT_NAME
 #lib 

 LINK_COMPONENTS
 Core
 Support 

 PLUGIN_TOOL 
 opt
 )
#add_library (AndersenObj OBJECT ${AndersenSourceCodes})
#add_library (Andersen SHARED $<TARGET_OBJECTS:AndersenObj>)
#add_library (AndersenStatic STATIC $<TARGET_OBJECTS:AndersenObj>)
#target_link_libraries (AndersenStatic LLVMCore LLVMSupport)
