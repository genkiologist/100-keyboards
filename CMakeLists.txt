if(CONFIG_SHIELD_100_KEYBOARDS_CENTRAL)
  zephyr_library()

  # ZMK本体のヘッダーファイルを参照できるようにインクルードパスを追加
  zephyr_include_directories(${ZEPHYR_BASE}/../app/include)

  zephyr_library_sources(src/board.c)
endif()
