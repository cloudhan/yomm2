# Copyright (c) 2018-2020 Jean-Louis Leroy
# Distributed under the Boost Software License, Version 1.0.
# See accompanying file LICENSE_1_0.txt
# or copy at http://www.boost.org/LICENSE_1_0.txt)

add_library(yomm2 STATIC yomm2.cpp)

target_include_directories(yomm2 PUBLIC
  $<BUILD_INTERFACE:${YOMM2_SOURCE_DIR}/include>
  $<INSTALL_INTERFACE:include>
)
target_include_directories(yomm2 SYSTEM PUBLIC ${Boost_INCLUDE_DIR})

install(TARGETS yomm2
  EXPORT YOMM2Targets
  LIBRARY DESTINATION lib
  ARCHIVE DESTINATION lib
)
