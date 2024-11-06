cmake_minimum_required(VERSION 3.16)

project(libzmodem LANGUAGES C)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(zmodem SHARED
  crctab.c
  crctab.h
  gettext.h
  log.h
  log.c
  lrz.c
  lsz.c
  protname.c
  rbsb.c
  tcp.c
  timing.h timing.c
  zglobal.h
  zm.c
  zm.h
  _zmodem.h
  zreadline.c
)

target_compile_definitions(zmodem PRIVATE LIBZMODEM_LIBRARY)

add_executable(msz msz.c)
target_link_libraries(msz zmodem)

add_executable(mrz mrz.c)
target_link_libraries(mrz zmodem)

#include(GNUInstallDirs)
set(CMAKE_INSTALL_LIBDIR /usr/lib)
set(CMAKE_INSTALL_BINDIR /usr/bin)

install(TARGETS zmodem msz mrz
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)

install(FILES zmodem.h DESTINATION /usr/include)








