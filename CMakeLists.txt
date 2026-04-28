if(CONFIG_SHIELD_100_KEYBOARDS_CENTRAL)
  zephyr_library()

  # GitHub Actionsの環境でもパスが通るように修正
  if (NOT DEFINED WEST_TOPDIR)
    set(WEST_TOPDIR ${CMAKE_CURRENT_SOURCE_DIR}/..)
  endif()

  # ZMKのapp/includeディレクトリを明示的に追加
  zephyr_include_directories(${WEST_TOPDIR}/zmk/app/include)

  zephyr_library_sources(src/board.c)
endif()
