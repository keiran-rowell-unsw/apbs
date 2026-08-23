set(EXECUTABLE_OUTPUT_PATH ${TOOLS_PATH}/bin)

if(ENABLE_FETK)
    add_subdirectory(mesh)
    add_subdirectory(manip)
else()
    message(STATUS "Skipping tools/mesh and tools/manip because ENABLE_FETK=OFF")
endif()

if(ENABLE_PYTHON)
    add_subdirectory(python)
    add_subdirectory(python-pybind)
endif(ENABLE_PYTHON)

unset(EXECUTABLE_OUTPUT_PATH)
