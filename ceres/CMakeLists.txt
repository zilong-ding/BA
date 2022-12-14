

aux_source_directory(${PROJECT_SOURCE_DIR}/ceres SRC_LIST)
find_package(Ceres REQUIRED)
add_executable(bundle_adjustment_ceres ${SRC_LIST})
target_link_libraries(bundle_adjustment_ceres ${CERES_LIBRARIES} ${PROJECT_SOURCE_DIR}/build/lib/libbal.a)