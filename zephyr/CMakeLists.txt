if(CONFIG_LIBSAMPLE)
  add_subdirectory(.. build)

  zephyr_include_directories(../include)
endif()
