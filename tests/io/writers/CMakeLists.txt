SET(DGTAL_TESTS_SRC_IO_WRITERS
       testCompressedVolWriter
       testPNMRawWriter 
       testMeshWriter
       testGenericWriter)


FOREACH(FILE ${DGTAL_TESTS_SRC_IO_WRITERS})
  add_executable(${FILE} ${FILE})
  target_link_libraries (${FILE} DGtal)
  add_test(${FILE} ${FILE})
ENDFOREACH(FILE)
