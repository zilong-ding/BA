aux_source_directory(${PROJECT_SOURCE_DIR}/g2o SRC_LIST)
#set(G2O_ROOT /usr/local/include/g2o)
LIST(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)
find_package(G2O REQUIRED)
find_Package(CSparse REQUIRED)
include_directories(${CSPARSE_INCLUDE_DIR})
SET(G2O_LIBS g2o_csparse_extension g2o_stuff g2o_core cxsparse)
add_executable(bundle_adjustment_g20 ${SRC_LIST})
target_link_libraries(bundle_adjustment_g20 ${PROJECT_SOURCE_DIR}/build/lib/libbal.a ${G2O_LIBS})