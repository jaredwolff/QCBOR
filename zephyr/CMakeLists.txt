if(CONFIG_QCBOR)
zephyr_compile_definitions(QCBOR_DISABLE_PREFERRED_FLOAT)
zephyr_compile_definitions(QCBOR_DISABLE_FLOAT_HW_USE)
zephyr_compile_definitions(QCBOR_CONFIG_DISABLE_EXP_AND_MANTISSA)

zephyr_include_directories(../inc)

zephyr_library()
zephyr_library_sources(../src/qcbor_decode.c)
zephyr_library_sources(../src/qcbor_encode.c)
zephyr_library_sources(../src/qcbor_err_to_str.c)
zephyr_library_sources(../src/UsefulBuf.c)
endif()