add_executable(WPELauncher
    main.cpp
)

target_include_directories(WPELauncher PUBLIC
    ${GLib_INCLUDE_DIRS}
    ${WPE_WEBKIT_INCLUDE_DIRS}
)
target_link_libraries(WPELauncher
    ${GLib_LIBRARIES}
    ${WPE_WEBKIT_LIBRARIES}
)

install(TARGETS WPELauncher DESTINATION "${CMAKE_INSTALL_PREFIX}/bin")
