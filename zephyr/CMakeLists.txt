if(CONFIG_QCBOR)
set(QCBOR_DIR ${ZEPHYR_CURRENT_MODULE_DIR})

zephyr_compile_definitions(QCBOR_DISABLE_PREFERRED_FLOAT)
zephyr_compile_definitions(QCBOR_DISABLE_FLOAT_HW_USE)
zephyr_compile_definitions(QCBOR_CONFIG_DISABLE_EXP_AND_MANTISSA)

zephyr_library()

zephyr_include_directories(${QCBOR_DIR}/inc)

zephyr_library_sources(${QCBOR_DIR}/src/qcbor_decode.c)
zephyr_library_sources(${QCBOR_DIR}/src/qcbor_encode.c)
zephyr_library_sources(${QCBOR_DIR}/src/qcbor_err_to_str.c)
zephyr_library_sources(${QCBOR_DIR}/src/UsefulBuf.c)
endif()

