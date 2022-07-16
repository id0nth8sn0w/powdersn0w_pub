INCLUDE(FindOpenSSL)

add_library(asr asr.c)
target_link_libraries(asr common ${OPENSSL_LIBRARIES})
include_directories(${OPENSSL_INCLUDE_DIR})
