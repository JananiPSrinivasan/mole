# mole_C++ Library Configuration
set(SOURCES utils.cpp divergence.cpp gradient.cpp laplacian.cpp interpol.cpp mixedbc.cpp robinbc.cpp)

add_library(mole_C++ ${SOURCES})
target_include_directories(mole_C++ PUBLIC ${ARMADILLO_INCLUDE_DIRS} ${EIGEN3_INCLUDE_DIRS} ${OpenBLAS_INCLUDE_DIRS} ${SUPERLU_INCLUDE_DIR})
target_link_libraries(mole_C++ PUBLIC ${LINK_LIBS})

# Installation for mole library
install(TARGETS mole_C++ DESTINATION "${CMAKE_BINARY_DIR}/install")
