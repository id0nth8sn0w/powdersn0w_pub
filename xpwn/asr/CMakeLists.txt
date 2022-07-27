add_library(asr asr.c)
target_link_libraries(asr common)
include_directories(${OPENSSL_INCLUDE_DIR})
