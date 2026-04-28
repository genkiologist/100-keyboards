if(CONFIG_SHIELD_100_KEYBOARDS_CENTRAL)
  zephyr_library()
  zephyr_library_sources(src/board.c)
endif()
